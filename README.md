```markdown
# OpenManus

OpenManus is an open-source framework for building general AI agents without restrictions.

---

## Installation

### Method 1: Using Conda

1. Create and activate a new environment:
   ```bash
   conda create -n open_manus python=3.12
   conda activate open_manus
   ```
2. Clone the repository and install dependencies:
   ```bash
   git clone https://github.com/mannaandpoem/OpenManus.git
   cd OpenManus
   pip install -r requirements.txt
   ```

### Method 2: Using uv (Recommended)

1. Install `uv`:
   ```bash
   curl -LsSf https://astral.sh/uv/install.sh | sh
   ```
2. Clone the repository:
   ```bash
   git clone https://github.com/mannaandpoem/OpenManus.git
   cd OpenManus
   ```
3. Create and activate a virtual environment with Python 3.12:
   ```bash
   uv venv --python 3.12
   source .venv/bin/activate    # Unix/macOS
   # .venv\Scripts\activate     # Windows
   ```
4. Install dependencies:
   ```bash
   uv pip install -r requirements.txt
   ```

#### (Optional) Browser Automation

If you plan to use Playwright for browser automation:
```bash
playwright install
```

---

## Configuration

1. Copy the example configuration file:
   ```bash
   cp config/config.example.toml config/config.toml
   ```
2. Open `config/config.toml` in your editor and update your API credentials and settings. For example:
   ```toml
   [llm]
   model       = "gpt-4o"
   base_url    = "https://api.openai.com/v1"
   api_key     = "sk-..."        # Replace with your API key
   max_tokens  = 4096
   temperature = 0.0
   ```

---

## Usage

- **Run the main agent**  
  ```bash
  python main.py
  ```
- **Other tools**  
  ```bash
  python run_mcp.py    # MCP tool version
  python run_flow.py   # Experimental multi-agent version
  ```

---

## Contributing

We welcome issues, feature requests, and pull requests!

1. Fork the repo and create your feature branch.
2. Commit your changes with clear messages.
3. Run pre-commit checks before submitting a PR:
   ```bash
   pre-commit run --all-files
   ```
4. Push to your fork and open a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```
