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

### Cross-Platform Support

This project supports both Linux and Windows:

- **Linux**: Full CUDA support with GPU acceleration (all NVIDIA CUDA packages installed automatically)
- **Windows**: Automatic exclusion of Linux-only CUDA packages that don't have Windows wheels

The project uses UV's constraint-dependencies feature to automatically handle platform-specific dependencies:
- CUDA packages (`nvidia-cufile-cu12`, `triton`, etc.) are only installed on Linux systems
- Windows installations automatically skip incompatible packages
- No manual intervention required - `uv sync` works on both platforms

### Requirements

- Python 3.12+
- uv (install with `pip install uv`)

The project includes dependencies for:
- marker-pdf (PDF processing)
- JupyterLab (interactive notebooks)  
- PyTorch ecosystem (ML/AI with platform-appropriate CUDA support)
- Various data science libraries (pandas, numpy, matplotlib, etc.)

### Optional CUDA Dependencies

Linux users can also explicitly install additional CUDA dependencies if needed:

```bash
uv sync --extra cuda
```

This is typically not necessary as the required CUDA packages are automatically installed on Linux.