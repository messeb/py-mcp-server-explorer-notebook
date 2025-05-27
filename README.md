# 🔎 MCP Server Explorer Notebook

An interactive notebook environment to explore, list, and invoke tools from MCP (Model Context Protocol) servers using [`fastmcp`](https://pypi.org/project/fastmcp/) and [`fast-agent-mcp`](https://pypi.org/project/fast-agent-mcp/).

Ideal for building and testing tool-driven AI agents using LLMs like OpenAI or Claude, augmented by external tool servers like Playwright and Brave Search.


## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/messeb/py-mcp-server-explorer-notebook.git
cd py-mcp-server-explorer-notebook
```


## 🔐 Environment Setup

### 2️⃣ Set Up Your API Keys

Rename the provided `example.env` to `.env`:

```bash
mv example.env .env
```

Edit `.env` and fill in your API keys:

```bash
# .env
ANTHROPIC_API_KEY=your_claude_key
OPENAI_API_KEY=your_openai_key
BRAVE_API_KEY=your_brave_key
```


## ⚙️ FastAgent Configuration

### 3️⃣ Configure fastagent.config

Rename `example.fastagent.config` to `fastagent.config.yaml`:

```bash
mv example.fastagent.config fastagent.config.yaml
```

Edit the config to include your environment variables (e.g. for Brave Search):

```yaml
mcp:
  servers:
    brave_websearch:
      command: npx
      args: ["-y", "@modelcontextprotocol/server-brave-search"]
      env:
        BRAVE_API_KEY: "<KEY>"
```


## 📒 Run the Notebook

Open [mcp-server-explorer-notebook.ipynb](./mcp-server-explorer-notebook.ipynb) to:

- List available tools from MCP servers
- Call tools directly (e.g. Brave Search, Playwright)
- Route tool usage through an LLM using `FastAgent`


## 🧠 Credits

Powered by:

- [fast-agent-mcp](https://github.com/evalstate/fast-agent)
- [fastmcp](https://github.com/jlowin/fastmcp)
- [OpenAI](https://platform.openai.com/)
- [Anthropic Claude](https://www.anthropic.com/)
- [Brave Search API](https://brave.com/search/api/)
