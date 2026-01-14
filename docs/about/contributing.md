# Contributing

Thank you for considering contributing to our documentation! This guide will help you get started.

## How to Contribute

There are many ways to contribute:

- **Report Issues**: Found a typo or error? Let us know!
- **Suggest Improvements**: Have ideas for better documentation?
- **Write Content**: Add new pages or improve existing ones
- **Fix Bugs**: Correct errors in code examples
- **Translate**: Help translate docs to other languages

## Getting Started

### 1. Fork the Repository

Click the "Fork" button on our GitHub repository to create your own copy.

### 2. Clone Your Fork

```bash
git clone https://github.com/YOUR_USERNAME/project-name.git
cd project-name
```

### 3. Create a Branch

```bash
git checkout -b feature/your-feature-name
```

### 4. Make Your Changes

Edit the Markdown files in the `docs/` directory.

### 5. Test Locally

Run the development server to preview your changes:

```bash
mkdocs serve
```

Visit `http://127.0.0.1:8000/` to see your changes.

### 6. Commit Your Changes

```bash
git add .
git commit -m "Add: description of your changes"
```

### 7. Push to GitHub

```bash
git push origin feature/your-feature-name
```

### 8. Create a Pull Request

Go to the original repository and click "New Pull Request".

## Contribution Guidelines

### Documentation Style

!!! info "Writing Style"
    - Use clear, concise language
    - Write in present tense
    - Use active voice
    - Keep paragraphs short (3-5 sentences)
    - Use headings to organize content

### Code Examples

All code examples should:

- Be tested and working
- Include comments for complex logic
- Follow language-specific conventions
- Include expected output when relevant

Example:

```python
# Good example with clear comments
def calculate_total(items):
    """Calculate the total price of items."""
    return sum(item.price for item in items)

# Usage
total = calculate_total(cart_items)
print(f"Total: ${total}")  # Total: $150.00
```

### Markdown Conventions

- Use `#` for headings (not underlines)
- Use fenced code blocks with language specification
- Use relative links for internal pages
- Include alt text for all images

### Commit Messages

Follow this format:

```
Type: Brief description

Detailed explanation if needed.

Closes #issue_number
```

Types:
- `Add`: New content
- `Update`: Modify existing content
- `Fix`: Correct errors
- `Remove`: Delete content
- `Docs`: Documentation-only changes

Examples:

```
Add: Getting started tutorial

Updated the getting started section with a comprehensive tutorial
including installation steps and first project setup.

Closes #42
```

## Review Process

1. **Automated Checks**: CI runs automated tests
2. **Peer Review**: Maintainers review your changes
3. **Feedback**: Address any requested changes
4. **Approval**: Once approved, your PR will be merged

!!! tip "Review Tips"
    - Respond promptly to feedback
    - Be open to suggestions
    - Ask questions if unclear
    - Test all changes thoroughly

## Code of Conduct

### Our Pledge

We pledge to make participation in our community a harassment-free experience for everyone, regardless of:

- Age, body size, disability
- Ethnicity, gender identity and expression
- Level of experience, education
- Nationality, personal appearance
- Race, religion, sexual orientation

### Expected Behavior

- Be respectful and inclusive
- Accept constructive criticism
- Focus on what's best for the community
- Show empathy towards others

### Unacceptable Behavior

- Harassment or discriminatory comments
- Trolling or insulting remarks
- Personal or political attacks
- Publishing others' private information
- Other conduct deemed inappropriate

## Recognition

Contributors are recognized in several ways:

- Listed in the [Contributors](https://github.com/project/graphs/contributors) page
- Mentioned in release notes
- Featured in the documentation

## Questions?

Need help getting started?

- Check existing issues and pull requests
- Read our [documentation](../getting-started/introduction.md)
- Join our community forum
- Email us at contributors@example.com

## Resources

- [Markdown Guide](https://www.markdownguide.org/)
- [MKDocs Documentation](https://www.mkdocs.org/)
- [Material Theme Docs](https://squidfunk.github.io/mkdocs-material/)

---

!!! success "Thank You!"
    Every contribution, no matter how small, makes a difference. We appreciate your help in making our documentation better!

| Company  | Supported? | Notes |
| -------- | ---------- | ----- |
| Venafi   | Yes        |       |
| CyberArk | Yes        |       |
| PAN      | No         |       |
|          |            |       |

