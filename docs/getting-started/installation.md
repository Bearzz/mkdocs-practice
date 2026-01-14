# Installation

This guide walks you through the installation process step by step.

## System Requirements

Before installing, ensure your system meets these requirements:

| Requirement | Minimum Version |
|------------|----------------|
| Python | 3.7+ |
| pip | Latest version |
| Operating System | Windows, macOS, Linux |

## Installation Steps

### Step 1: Install Python

=== "Windows"
    Download Python from [python.org](https://www.python.org/) and run the installer.

    ```bash
    # Verify installation
    python --version
    ```

=== "macOS"
    Python 3 comes pre-installed on macOS. To get the latest version:

    ```bash
    brew install python3
    python3 --version
    ```

=== "Linux"
    ```bash
    sudo apt update
    sudo apt install python3 python3-pip
    python3 --version
    ```

### Step 2: Install MKDocs

Install MKDocs using pip:

```bash
pip install mkdocs
```

Verify the installation:

```bash
mkdocs --version
```

### Step 3: Install Material Theme

Install the Material theme for MKDocs:

```bash
pip install mkdocs-material
```

!!! success "Installation Complete"
    You've successfully installed MKDocs with Material theme!

## Verification

To verify everything is working correctly:

```bash
# Create a test project
mkdocs new test-project
cd test-project

# Start the development server
mkdocs serve
```

Open your browser to `http://127.0.0.1:8000/` to see your documentation site.

## Troubleshooting

!!! warning "Common Issues"

    **Issue**: `mkdocs: command not found`

    **Solution**: Add Python's bin directory to your PATH

    ---

    **Issue**: Permission denied errors

    **Solution**: Use `pip install --user mkdocs mkdocs-material`

## Next Steps

Now that you have everything installed, proceed to the [Quick Start](quickstart.md) guide to create your first documentation site!
