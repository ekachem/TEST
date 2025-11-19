## Markdown Syntax Documentation
### 1. Headings
Headings are used to structure your document hierarch from main titles to sub-sections.
markdown
```
# H1: Largest Heading (Document Title)
## H2: Second largest
### H3: Third largest
#### H4: Fourth largest
##### H5: Fifth largest
###### H6: Smallest heading
```

### 2. Paragraphs and Line Breaks
Paragraphs are created by using one or more blank lines between lines of text.
```
markdown
This is the first line of a paragraph.
You can write several sentences here.

This is a new paragraph entirely.

To force a manual line break within the same paragraph,
end a line with two spaces or a backslash\ 
followed by hitting the Return key.
```

### 3. Text Formatting (Emphasis)
You can emphasize text using asterisks (*) or underscores (_).
```
markdown
*Italics* or _italics_
**Bold text** or __bold text__
***Bold and italics together***
~~Strikethrough text~~ (often supported)
Use code with caution.
```

### 4. Lists
Markdown supports both ordered (numbered) and unordered (bulleted) lists.
```
markdown
**Unordered List:**

* Item 1
* Item 2
    * Nested item A
    * Nested item B
* Item 3

**Ordered List:**

1. First item
2. Second item
3. Third item
    1. Nested number list
    2. Continues counting
```

### 5. Links
Create inline links using square brackets for the link text and parentheses for the URL.
```
markdown
Visit [Google](https://www.google.com) for searching.
You can also use relative links like [local-file](./local-file.md).
```

### 6. Images
Images are similar to links but start with an exclamation point (!).

### 7. Fenced Code Block
Defines a Code Block: The triple backticks (```) mark the beginning and end of a section that should be treated as code, preserving formatting like indentation and line breaks.
Example markdown
Here is a simple Python code example:

```python
s = "Python syntax highlighting"
print(s)
```
