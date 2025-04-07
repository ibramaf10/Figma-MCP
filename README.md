🚀 Quick Installation with pipx
Install figma-mcp by running:


pipx install figma-mcp
⚙️ Configuration for Cursor
In the settings, add an MCP server using the following command:

 
figma-mcp --figma-api-key=your_figma_key
Alternatively, create a .cursor/mcp.json file in your project with the following content:

json 
{
  "mcpServers": {
    "figma-python": {
      "command": "figma-mcp",
      "args": [
        "--figma-api-key=your_figma_key"
      ]
    } 
  }
}
🖥️ Configuration for Other IDEs (e.g., Windsurf)
Use an MCP configuration file (e.g., mcp_config.json):

json 
{
  "mcpServers": {
    "figma-python": {
      "command": "figma-mcp",
      "args": [
        "--figma-api-key=your_figma_key"
      ]
    } 
  }
}
🔧 Install uv and Set Up the Environment
Run the following commands:

 
curl -LsSf https://astral.sh/uv/install.sh | sh
uv venv
source .venv/bin/activate
uv sync
🧪 Test Locally
Run the server with:

create .env

go get your figma api key

FIGMA_API_TOKEN=

 
python -m figma_mcp.main
