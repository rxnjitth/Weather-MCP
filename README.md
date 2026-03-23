# Weather

A simple Python project that provides a weather‑related MCP (Claude Agent) server and a client for interactive chat using Ollama.

## Features
- **MCP server** with tools:
  - `get_alerts(state)` – fetch active NWS weather alerts for a US state.
  - `greet_user(name, style)` – generate a friendly, formal or casual greeting.
  - `echo_resource(message)` – a demo echo resource.
- **Client** (`server/client.py`) that runs an interactive chat with built‑in conversation memory.

## Prerequisites
- Python 3.11 or newer
- [Ollama](https://ollama.com/) with the `llama3.2:latest` model available
- An OpenAI‑compatible API key is **not** required (the client uses Ollama locally)

## Installation
```bash
# Clone the repository (if you haven't already)
git clone <repo-url>
cd weather

# Create a virtual environment
python -m venv .venv
source .venv/bin/activate  # on Windows use ".venv\\Scripts\\activate"

# Install dependencies
pip install -r requirements.txt  # or `pip install -e .` if a pyproject build backend is set up
```

## Running the server
```bash
python -m server.weather  # registers the MCP tools
```
The server is automatically started when the module is imported by MCP.

## Running the interactive client
```bash
python -m server.client
```
You will see a prompt. Type your queries, e.g., `What is the weather in NY?` or `get_alerts CA`. Use `exit` or `quit` to leave, and `clear` to reset the conversation history.



## License
MIT – see the `LICENSE` file for details.
