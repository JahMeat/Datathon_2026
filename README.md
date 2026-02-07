# Datathon_2026
This is my project for UW DubsTech's 7th Annual Datathon!

## Setup

This project uses [UV](https://github.com/astral-sh/uv) as the Python package manager.

### Installing UV

#### macOS and Linux
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

#### Windows
```powershell
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

#### Using pip
```bash
pip install uv
```

### Project Setup

1. Clone the repository:
```bash
git clone https://github.com/JahMeat/Datathon_2026.git
cd Datathon_2026
```

2. Create a virtual environment and install dependencies:
```bash
uv sync
```

3. Activate the virtual environment:
```bash
source .venv/bin/activate  # On macOS/Linux
# or
.venv\Scripts\activate  # On Windows
```

### Adding Dependencies

To add new packages:
```bash
uv add package-name
```

To add development dependencies:
```bash
uv add --dev package-name
```

## Project Structure

- `Data/` - Directory for storing datasets and data files
- `pyproject.toml` - Project configuration and dependencies
- `.python-version` - Specifies the Python version for the project 
