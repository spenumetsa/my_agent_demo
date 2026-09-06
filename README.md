# My Agent Demo

## Project Overview

`my_agent_demo` is a lightweight demonstration of a conversational AI agent built with OpenAI's GPT‑4. The repository showcases how to structure a simple agent that can respond to user prompts, manage state, and be extended with custom tools. It serves as a learning resource for developers interested in building AI‑driven applications, experimenting with prompt engineering, or integrating language models into existing workflows.

## Features

- **Modular Architecture** – Core agent logic is separated from tool implementations, making it easy to add or replace functionality.
- **Extensible Tooling** – Includes a set of example tools (file handling, searching, branch management) that can be expanded.
- **Clear Documentation** – This README provides an overview, installation steps, usage examples, and contribution guidelines.

## Installation

### Prerequisites

- Python 3.9 or newer
- Access to the OpenAI API (API key)
- Git

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/my_agent_demo.git
   cd my_agent_demo
   ```
2. **Create a virtual environment** (optional but recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```
3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
4. **Configure your OpenAI API key**
   ```bash
   export OPENAI_API_KEY='sk-...'
   # Or add it to a .env file and load with python-dotenv
   ```

## Usage Examples

### Running the Agent Interactively

```bash
python -m my_agent_demo
```
You will be prompted to enter messages. The agent will respond using the GPT‑4 model.

### Using Built‑in Tools

The agent can invoke tools such as `read_file`, `create_file`, and `search_code`. Example interaction:

```
User: Show me the contents of `my_agent_demo/__init__.py`.
Agent: (invokes `read_file` tool)
```

### Extending with Custom Tools

1. Create a new file in `my_agent_demo/tools/` implementing the desired functionality.
2. Register the tool in `my_agent_demo/agent.py` under the `tools` dictionary.
3. The agent will automatically be able to call the new tool via natural language prompts.

## Contribution Guidelines

We welcome contributions! Please follow these steps:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes** – ensure code follows the existing style and includes tests where applicable.
4. **Run the test suite**
   ```bash
   pytest
   ```
5. **Commit your changes** with a clear commit message.
6. **Push to your fork** and open a Pull Request against the `main` branch.

### Code Style

- Use `black` for formatting.
- Follow PEP 8 naming conventions.
- Add docstrings to all public functions and classes.

### Reporting Issues

If you encounter a bug or have a feature request, please open an issue with:
- A clear description
- Steps to reproduce (if applicable)
- Expected vs. actual behavior

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

*Happy hacking!*