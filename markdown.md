# Markdown Cheat Sheet
*Quick Reference for Beginners*

## What is Markdown?
Markdown is a simple way to format text using plain text characters. It's used for README files, documentation, and notes.

---

## Headers
Use `#` symbols with a space:

```markdown
# Main Title (biggest)
## Section Header 
### Subsection Header
#### Smaller Header
```

**Result:**
# Main Title
## Section Header 
### Subsection Header

---

## Text Formatting

```markdown
**Bold text**
*Italic text*
`Code or technical terms`
```

**Result:**
**Bold text**  
*Italic text*  
`Code or technical terms`

---

## Lists

**Bullet Lists:**
```markdown
- First item
- Second item
  - Nested item (2 spaces before dash)
  - Another nested item
- Third item
```

**Numbered Lists:**
```markdown
1. First step
2. Second step
3. Third step
```

---

## Links and Images

**Links:**
```markdown
[Link text](https://example.com)
[Python documentation](https://python.org)
```

**Images:**
```markdown
![Description of image](image-file.png)
![Sales chart](charts/sales-2024.png)
```

---

## Code

**Inline code:**
```markdown
Use the `pandas.read_csv()` function to load data.
```

**Code blocks:**
````markdown
```python
import pandas as pd
df = pd.read_csv("data.csv")
print(df.head())
```
````

---

## Tables

```markdown
| Name        | Age | City        |
|-------------|-----|-------------|
| John Smith  | 25  | New York    |
| Jane Doe    | 30  | Chicago     |
| Bob Johnson | 35  | Los Angeles |
```

**Result:**
| Name        | Age | City        |
|-------------|-----|-------------|
| John Smith  | 25  | New York    |
| Jane Doe    | 30  | Chicago     |
| Bob Johnson | 35  | Los Angeles |

---

## Quotes

```markdown
> This is a quote or important note.
> It can span multiple lines.
```

**Result:**
> This is a quote or important note.
> It can span multiple lines.

---

## Line Breaks

- Leave a **blank line** between paragraphs
- Add **two spaces** at the end of a line for a line break  
- Use `---` for a horizontal line

---

## Quick Tips

- **Preview your work** - most editors show a preview
- **Spacing matters** - always put a space after `#` and `-`
- **File names** - save as `.md` (like `report.md`)
- **Keep it simple** - markdown should be readable even as plain text

---

## Common File Names
- `README.md` - project description
- `notes.md` - class or meeting notes  
