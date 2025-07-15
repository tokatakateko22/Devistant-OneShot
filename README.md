# Devistant

Devistant is an automated SDLC (Software Development Life Cycle) workflow tool that leverages multiple AI agents and LLMs to guide you through requirements analysis, planning, project management, use case generation, class diagramming, database design, and documentation for software projects.

## Features
- **Multi-phase SDLC automation**: Covers requirements, planning, project management, use cases, class diagrams, database design, and documentation.
- **Agent-based workflow**: Each SDLC phase is handled by a specialized agent.
- **LLM integration**: Uses local or remote LLMs (e.g., via Ollama) for natural language processing and generation.
- **Automatic project documentation**: Generates structured documentation for your project.
- **Jupyter Notebook interface**: Interactive and easy to use.

## Setup Instructions
1. **Python Requirements**:
   - Python 3.10+
   - Jupyter Notebook or JupyterLab

2. **Install dependencies**:
   - Install required Python packages:
     ```bash
     pip install langgraph langchain langchain_community langchain_core langchain_openai langchain_groq
     pip install typing_extensions python-dotenv
     ```
   - (You may need additional packages depending on your LLM backend.)

3. **LLM Backend**:
   - This project expects an LLM backend such as [Ollama](https://ollama.com/) running locally with models like `phi4`, `llama2`, or similar.
   - Start Ollama and pull the required models:
     ```bash
     ollama pull phi4
     ollama pull llama2
     # ...
     ```

4. **Run the Notebook**:
   - Open `Devistant.ipynb` in Jupyter Notebook or JupyterLab.
   - Follow the instructions in the notebook to start the SDLC workflow.

## Usage Example
1. Open the notebook and run all cells.
2. The workflow will prompt you for a project description and automatically proceed through all SDLC phases, generating outputs for each.
3. Outputs include requirements, plans, management strategies, use cases, diagrams, and documentation.

## Troubleshooting
- **AttributeError: 'dict' object has no attribute ...**
  - Make sure all code uses `project_memory.get('key')` for dictionary access, not dot notation.
- **Model is slow or stuck**
  - Use a smaller LLM model or check your system resources.
- **Ollama not responding**
  - Ensure the Ollama server is running and the required models are pulled.
- **Other errors**
  - Check that all dependencies are installed and compatible with your Python version.

## License
MIT License 