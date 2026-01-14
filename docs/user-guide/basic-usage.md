# Basic Usage

Learn the fundamental operations and everyday tasks.

## Getting Started with Basic Operations

This page covers the core functionality you'll use regularly.

## Core Concepts

### Configuration

All configuration is done through the `mkdocs.yml` file:

```yaml
site_name: My Site
theme:
  name: material
nav:
  - Home: index.md
  - Guide: guide.md
```

### Writing Content

Content is written in Markdown format:

```markdown
# Main Heading

This is a paragraph with **bold** and *italic* text.

- List item 1
- List item 2

1. Numbered item
2. Another item
```

## Common Tasks

### Task 1: Creating a New Page

**Step 1**: Create a new `.md` file in the `docs/` directory

```bash
touch docs/new-page.md
```

**Step 2**: Add content to your page

```markdown
# My New Page

This is the content of my new page.
```

**Step 3**: Add it to navigation in `mkdocs.yml`

```yaml
nav:
  - Home: index.md
  - New Page: new-page.md
```

!!! success "Page Created"
    Your new page is now accessible in the navigation menu!

### Task 2: Adding Images

Place images in your `docs/` directory and reference them:

```markdown
![Alt text](images/my-image.png)
```

With a caption:

```markdown
![Alt text](images/my-image.png)
*Figure 1: Image caption*
```

### Task 3: Creating Links

Internal links to other pages:

```markdown
[Link text](other-page.md)
[Getting Started](getting-started/introduction.md)
```

External links:

```markdown
[Google](https://www.google.com)
```

### Task 4: Adding Code Blocks

Inline code: \`code here\`

Block code with syntax highlighting:

    ```python
    def hello_world():
        print("Hello, World!")
    ```

## Content Features

### Admonitions

Create callout boxes for important information:

!!! note "Note Title"
    This is a note with important information.

!!! warning "Warning"
    This is a warning message.

!!! tip "Pro Tip"
    This is a helpful tip!

### Tables

Create tables for structured data:

| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Row 1    | Data     | More data|
| Row 2    | Data     | More data|

### Lists

Unordered lists:

- Item 1
- Item 2
  - Nested item
  - Another nested item
- Item 3

Ordered lists:

1. First step
2. Second step
3. Third step

## Best Practices

!!! success "Tips for Success"
    - Keep pages focused on a single topic
    - Use descriptive headings
    - Include code examples where appropriate
    - Add images to clarify complex concepts
    - Link to related pages
    - Keep paragraphs short and readable

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl/Cmd + K` | Open search |
| `/` | Focus search |
| `←` `→` | Navigate pages |

## Next Steps

Once you're comfortable with basic usage, explore [Advanced Features](advanced-features.md) to unlock more powerful capabilities!

---

!!! question "Need Help?"
    If you're stuck, check the [API Reference](../api/overview.md) or search the documentation.
