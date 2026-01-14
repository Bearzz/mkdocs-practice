# MKDocs Practice Documentation

A comprehensive documentation site built with MKDocs and Material theme.

## Features

- 🎨 Beautiful Material Design theme
- 🌓 Light/Dark mode toggle
- 🔍 Full-text search
- 📱 Fully responsive
- ⚡ Instant page loading
- 🔗 Previous/Next navigation
- 📋 Code copy buttons
- 🎯 Integrated table of contents

## Project Structure

```
mkdocs-practice/
├── docs/              # Documentation source files
│   ├── index.md       # Homepage
│   ├── getting-started/
│   ├── user-guide/
│   ├── api/
│   └── about/
├── mkdocs.yml         # MKDocs configuration
└── README.md          # This file
```

## Getting Started

### Prerequisites

- Python 3.7+
- pip

### Installation

1. Clone this repository:
```bash
git clone <repository-url>
cd mkdocs-practice
```

2. Install dependencies:
```bash
pip install mkdocs mkdocs-material
```

### Development

Start the development server:
```bash
mkdocs serve
```

Visit `http://127.0.0.1:8000/` in your browser.

### Build

Build the static site:
```bash
mkdocs build
```

The built site will be in the `site/` directory.

### Deploy

Deploy to GitHub Pages:
```bash
mkdocs gh-deploy
```

## Documentation Sections

- **Getting Started**: Introduction, Installation, Quick Start
- **User Guide**: Overview, Basic Usage, Advanced Features
- **API Reference**: Overview, Functions
- **About**: Contributing, License

## Built With

- [MKDocs](https://www.mkdocs.org/) - Static site generator
- [Material for MKDocs](https://squidfunk.github.io/mkdocs-material/) - Material theme

## License

This project is licensed under the MIT License - see the [License](docs/about/license.md) page for details.

## Contributing

Contributions are welcome! See the [Contributing Guide](docs/about/contributing.md) for details.
