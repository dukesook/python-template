# python-template

Starting point for a new python project

## Virtual Environment

### Create a Virtual Environment

```
python -m venv .venv
```

### Activate the Environment

```sh
source .venv/bin/activate     # Linux/macOS
.venv\Scripts\activate.bat    # Windows CMD
.\.venv\Scripts\Activate.ps1  # PowerShell
```

Once active, the virtual environment will only last for just that terminal session. VSCode has a feature that will activate automatically: `python.terminal.activateEnvironment`

### Verify Virtual Environment is Active

```sh
which python
# /usr/bin/python -> inactive
# /.../project-root/.venv/bin/python -> active
```

## File Structure

The Python Packaging Authority (PyPA) recommends:

```
my-project/                  # Repository root (can use hyphens)
├── pyproject.toml           # Build system, dependencies, and tool configs
├── README.md                # Project documentation
├── src/                     # Container directory (never has an __init__.py)
│   └── my_project/          # Importable package (must use underscores)
│       ├── __init__.py      # Signals this directory is an importable package
│       ├── __main__.py      # Runs when calling: python -m my_project (for executables)
│       ├── core.py
│       └── utils.py
└── tests/                   # Test suite isolated from source code
    ├── __init__.py
    └── test_utils.py
```

## Dependencies

### Install Package

Reads the pyproject.toml file

```
pip install -e .
```

### Run

```sh
python -m my_project  # -m = module
```
