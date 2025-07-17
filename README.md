# Coder Crew

A powerful AI-powered coding assistant built with [crewAI](https://crewai.com) that can write, execute, and debug Python code automatically. This project demonstrates how AI agents can collaborate to solve complex programming tasks with minimal human intervention.

## 🚀 Features

- **Automated Code Generation**: AI agents write Python code based on natural language descriptions
- **Code Execution & Testing**: Built-in execution and output validation
- **Intelligent Planning**: Agents plan their approach before writing code
- **Output Documentation**: Automatically generates comprehensive output files with code and results
- **Extensible Architecture**: Easy to customize agents, tasks, and tools

## 📋 Prerequisites

- Python >= 3.10, < 3.14
- [UV](https://docs.astral.sh/uv/) package manager
- OpenAI API key

## 🛠️ Installation

1. **Install UV** (if not already installed):
   ```bash
   pip install uv
   ```

2. **Clone and navigate to the project**:
   ```bash
   cd coder
   ```

3. **Install dependencies**:
   ```bash
   crewai install
   ```

4. **Set up environment variables**:
   Create a `.env` file in the project root and add your OpenAI API key:
   ```bash
   OPENAI_API_KEY=your_api_key_here
   ```

## 🎯 Quick Start

Run the coder crew with a simple command:

```bash
crewai run
```

This will execute the default task: calculating the first 10,000 terms of the series `1 - 1/3 + 1/5 - 1/7 + ...` multiplied by 4.

## 📁 Project Structure

```
coder/
├── src/coder/
│   ├── config/
│   │   ├── agents.yaml      # Agent definitions and configurations
│   │   └── tasks.yaml       # Task definitions and workflows
│   ├── tools/
│   │   └── custom_tool.py   # Custom tools for agents
│   ├── crew.py              # Main crew orchestration logic
│   └── main.py              # Entry point and execution
├── output/                  # Generated output files
├── knowledge/               # Knowledge base and context
└── tests/                   # Test files
```

## ⚙️ Configuration

### Agents (`src/coder/config/agents.yaml`)

The project uses a **Python Developer** agent with the following capabilities:
- **Role**: Python Developer
- **Goal**: Write clean, efficient Python code to solve assignments
- **Process**: Plan → Code → Execute → Validate
- **Model**: OpenAI GPT-4o

### Tasks (`src/coder/config/tasks.yaml`)

Tasks define what the agents will accomplish:
- **Description**: Natural language description of the coding task
- **Expected Output**: Specification of what should be produced
- **Output File**: Where results are saved (`output/code_and_output.txt`)

## 🔧 Customization

### Modifying the Assignment

Edit `src/coder/main.py` to change the coding assignment:

```python
assignment = 'Your custom coding task description here'
```

## 📊 Example Output

The coder crew generates comprehensive output files containing:
- Complete Python code
- Execution results
- Performance metrics
- Error handling and debugging information

Example output location: `output/code_and_output.txt`

