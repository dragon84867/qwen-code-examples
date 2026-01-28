# Qwen Excel Agent

> ⚠️ **IMPORTANT**: This is a demo application by Alibaba Cloud. It is intended for local development only and should NOT be deployed to production or used at scale.

A demonstration desktop application powered by Qwen and the [@qwen-code/sdk](https://github.com/QwenLM/qwen-code), showcasing AI-powered spreadsheet creation, analysis, and manipulation capabilities.

## What This Demo Shows

This Electron-based desktop application demonstrates how to:
- Create sophisticated Excel spreadsheets with formulas, formatting, and multiple sheets
- Analyze and manipulate existing spreadsheet data
- Use Qwen to assist with data organization and spreadsheet design
- Work with Python scripts to generate complex spreadsheet structures
- Integrate the @qwen-code/sdk with desktop applications

### Example Use Cases

The `agent/` folder contains Python examples including:
- **Workout Tracker**: A fitness log with automatic summary statistics and multiple sheets
- **Budget Tracker**: Financial tracking with formulas and data validation
- Custom spreadsheet generation with styling, borders, and conditional formatting

## Prerequisites

- [Node.js 20+](https://nodejs.org) or [Bun](https://bun.sh)
- [Qwen Code CLI](https://github.com/QwenLM/qwen-code) (installed locally)
- Local LLM service (such as [Ollama](https://ollama.ai) with a Qwen model)
- Python 3.9+ (for the Python agent examples)
- LibreOffice (optional, for formula recalculation)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/anthropics/sdk-demos.git
cd sdk-demos/excel-demo
```

2. Install dependencies:
```bash
npm install
# or bun install
```

3. Install Qwen Code CLI:
   ```bash
   npm install -g qwen-code
   ```

4. Set up a local LLM (recommended: Ollama):
   - Install [Ollama](https://ollama.ai)
   - Pull a Qwen model:
   ```bash
   ollama pull qwen2.5:7b
   ```

5. Optionally, configure your local model:
   - Set the `QWEN_CODE_MODEL` environment variable:
   ```bash
   export QWEN_CODE_MODEL="ollama/qwen2.5:7b"
   ```

6. Run the Electron application:
```bash
npm start
# or bun start
```

## Working with Python Examples

The `agent/` directory contains Python scripts demonstrating spreadsheet generation:

### Setup Python Environment

```bash
cd agent
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

### Run Example Scripts

```bash
# Create a workout tracker
python create_workout_tracker.py

# Create a budget tracker
python create_budget_tracker.py
```

See the [agent/README.md](./agent/README.md) for more details on the Excel agent setup and capabilities.

## Features

- **AI-Powered Spreadsheet Generation**: Let Qwen create complex spreadsheets based on your requirements
- **Formula Management**: Work with Excel formulas, calculations, and automatic recalculation
- **Professional Styling**: Generate spreadsheets with headers, colors, borders, and formatting
- **Multi-Sheet Workbooks**: Create workbooks with multiple related sheets
- **Data Analysis**: Analyze existing spreadsheets and extract insights
- **Desktop Integration**: Native desktop application built with Electron

## Project Structure

```
excel-demo/
├── agent/              # Python examples and Excel agent setup
│   ├── create_workout_tracker.py
│   ├── create_budget_tracker.py
│   └── README.md       # Excel agent documentation
├── src/
│   ├── main/          # Electron main process
│   └── renderer/      # React UI components
└── package.json
```

## Resources

- [@qwen-code/sdk Documentation](https://github.com/QwenLM/qwen-code)
- [Electron Documentation](https://www.electronjs.org/docs/latest/)
- [openpyxl Documentation](https://openpyxl.readthedocs.io/) (Python library used)

## Support

This is a demo application provided as-is. For issues related to:
- **@qwen-code/sdk**: [SDK Documentation](https://github.com/QwenLM/qwen-code)
- **Demo Issues**: [GitHub Issues](https://github.com/QwenLM/qwen-code/issues)
- **API Questions**: [Alibaba Cloud Support](https://www.alibabacloud.com/support)

## License

MIT - This is sample code for demonstration purposes.

---

Built by Alibaba Cloud to demonstrate the [@qwen-code/sdk](https://github.com/QwenLM/qwen-code)
