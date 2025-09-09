# Marker-Workspace

A workspace for marker-pdf and related ML/data science tools.

## Requirements

- Python 3.12.11 (latest 3.12.x)
- uv for dependency management

## Setup

1. Install uv if you haven't already:
   ```bash
   pip install uv
   ```

2. Install Python 3.12.11 and create the environment:
   ```bash
   uv python install 3.12.11
   uv sync
   ```

3. Run Python with all dependencies available:
   ```bash
   uv run python
   ```

## Usage

- Run Python scripts: `uv run python your_script.py`
- Add new dependencies: `uv add package_name`
- Install dependencies for a new clone: `uv sync`
- Run the main module: `uv run python main.py`

The project uses Python 3.12.11 with all ML/data science dependencies including:
- marker-pdf for PDF processing
- PyTorch ecosystem (torch, torchvision, torchaudio)
- Jupyter Lab for notebooks
- Data science libraries (pandas, numpy, matplotlib, etc.)
- And many more...

All dependencies are managed by uv and specified in `pyproject.toml`.