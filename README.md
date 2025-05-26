OpenManus

OpenManus is an open-source framework for building general AI agents without restrictions.
Installation
Method 1: Using conda

conda create -n open_manus python=3.12
conda activate open_manus
git clone https://github.com/mannaandpoem/OpenManus.git
cd OpenManus
pip install -r requirements.txt

Method 2: Using uv (Recommended)

curl -LsSf https://astral.sh/uv/install.sh | sh
git clone https://github.com/mannaandpoem/OpenManus.git
cd OpenManus
uv venv --python 3.12
source .venv/bin/activate   # Unix/macOS
# .venv\Scripts\activate    # Windows
uv pip install -r requirements.txt

(Optional) For browser automation tool:

playwright install

Configuration

Copy example config and add your API keys:

cp config/config.example.toml config/config.toml

Edit config/config.toml:

[llm]
model = "gpt-4o"
base_url = "https://api.openai.com/v1"
api_key = "sk-..."  # Replace with your key
max_tokens = 4096
temperature = 0.0

Usage

Run the main program:

python main.py

Other tools:

python run_mcp.py       # MCP tool version
python run_flow.py      # Experimental multi-agent version

Contribution

Feel free to submit issues or pull requests.

Run pre-commit checks before PR:

pre-commit run --all-files
