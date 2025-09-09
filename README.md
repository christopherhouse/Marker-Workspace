# Marker-Workspace

A workspace for working with marker-pdf and related tools, using uv for Python dependency management.

## Setup

This project uses [uv](https://docs.astral.sh/uv/) for Python dependency management.

### Quick Start

```bash
# Install dependencies
uv sync

# Run Python with dependencies available
uv run python

# Add new dependencies
uv add package-name

# Run a script
uv run python your_script.py
```

### Platform Support

This project supports both Linux and Windows:

- **Linux**: Full CUDA support with GPU acceleration
- **Windows**: CPU-only mode (CUDA packages are automatically excluded)

The project automatically handles platform-specific dependencies:
- CUDA packages (nvidia-cufile-cu12, triton) are only installed on Linux
- Windows installations will use CPU-only versions of PyTorch

### Requirements

- Python 3.12+
- uv (install with `pip install uv`)

The project uses Python 3.12.11 and includes dependencies for:
- marker-pdf (PDF processing)
- JupyterLab (interactive notebooks)
- PyTorch ecosystem (ML/AI)
- Various data science libraries (pandas, numpy, matplotlib, etc.)

### Optional CUDA Dependencies

For Linux users who want explicit CUDA support, you can install the optional CUDA dependencies:

```bash
uv sync --extra cuda
```