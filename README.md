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

### Requirements

- Python 3.12+
- uv (install with `pip install uv`)

The project uses Python 3.12.11 and includes dependencies for:
- marker-pdf (PDF processing)
- JupyterLab (interactive notebooks)
- PyTorch ecosystem (ML/AI)
- Various data science libraries (pandas, numpy, matplotlib, etc.)