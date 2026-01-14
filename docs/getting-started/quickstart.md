# Quick Start

Get up and running in just a few minutes!

## Create Your First Site

### 1. Create a New Project

```bash
mkdocs new my-project
cd my-project
```

This creates a basic structure:

```
my-project/
    mkdocs.yml    # Configuration file
    docs/
        index.md  # Homepage
```

### 2. Configure Material Theme

Edit `mkdocs.yml`:

```yaml
site_name: My Documentation
theme:
  name: material
```

### 3. Start the Development Server

```bash
mkdocs serve
```

Your site is now available at `http://127.0.0.1:8000/`

!!! tip "Live Reloading"
    The development server automatically reloads when you save changes!

## Add Content

### Create a New Page

Create a new file in the `docs/` directory:

```bash
echo "# About" > docs/about.md
```

### Update Navigation

Add it to `mkdocs.yml`:

```yaml
nav:
  - Home: index.md
  - About: about.md
```

### Write Markdown Content

MKDocs uses standard Markdown syntax:

```markdown
# Heading 1
## Heading 2

**Bold text** and *italic text*

- List item 1
- List item 2

[Link text](https://example.com)

    Code block with indentation
```

## Build Your Site

When you're ready to publish:

```bash
mkdocs build
```

This generates a `site/` directory with static HTML files ready for deployment.

## Deployment Options

=== "GitHub Pages"
    ```bash
    mkdocs gh-deploy
    ```

=== "Netlify"
    1. Connect your repository
    2. Set build command: `mkdocs build`
    3. Set publish directory: `site`

=== "Custom Server"
    Upload the contents of the `site/` directory to your web server.

## Common Commands

| Command | Description |
|---------|-------------|
| `mkdocs new [dir]` | Create a new project |
| `mkdocs serve` | Start development server |
| `mkdocs build` | Build static site |
| `mkdocs gh-deploy` | Deploy to GitHub Pages |
| `mkdocs --help` | Show all commands |

## Next Steps

!!! success "You're Ready!"
    You now know the basics! Explore the [User Guide](../user-guide/overview.md) to learn about advanced features.

---

**Additional Resources:**

- [MKDocs Documentation](https://www.mkdocs.org/)
- [Material Theme Docs](https://squidfunk.github.io/mkdocs-material/)
- [Markdown Guide](https://www.markdownguide.org/)
