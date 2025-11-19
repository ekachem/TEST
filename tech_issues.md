## How to Fix environment variable issue
# Here are three reliable ways to ensure the environment variable reaches your Python script:
Option 1: Explicitly pass all environment variables to sbatch
Modify the line in your outer script that calls sbatch to explicitly export all current variables:
bash
## In your outer loop script
(
  cd "$dir"
  # ... (exports are already here)
  sbatch --export=ALL submit.sh
)
Use code with caution.

This ensures that the GAMMA_B variable present in the outer script's environment is exported to the sbatch job environment.
Option 2: Pass the variable as a command-line argument to the Python script
This approach avoids environment variable propagation issues entirely by passing the value directly to the Python script.
Modify your outer script to pass the value to submit.sh, and then have submit.sh pass it to the Python script.
Modify submit.sh to accept an argument and pass it to Python.
Option 3: Set variables within submit.sh
A very robust method is to modify your outer script to pass the values as arguments to sbatch, which can then be read by submit.sh using the #SBATCH --export directive.
Modify your outer script:
bash
# In your outer loop script
```python
(
  cd "$dir"
  # Use sbatch environment variables flags
  sbatch --export=START_DIABAT=$st,GAMMA_B=$gam,I_COL=$icol,I_FRIC=$ifric submit.sh
)
Use code with caution.

Then, your submit.sh script should automatically have these variables available when the job starts.
A Note on Handling Missing Variables in Python
While fixing the shell script propagation is the primary solution, you can make your Python script more robust by providing a default value or handling the NoneType explicitly:
python
import os
# ... other imports

gmb = os.environ.get("GAMMA_B", "0.0") # Use a default value if not found
try:
    S["gamma_B"] = float(gmb)
except (ValueError, TypeError):
    print(f"Error: GAMMA_B environment variable not set or invalid: '{gmb}'")
    # Handle the error gracefully, maybe exit the script
    exit(1)
