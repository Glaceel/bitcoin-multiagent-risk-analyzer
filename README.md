# Autonomous Multi-Agent System for Bitcoin Technical Analysis & Portfolio Risk Management

An advanced AI orchestrator built on Langflow that utilizes a Multi-Agent architecture to process structured financial data (.csv) and deliver autonomous risk management recommendations without numerical hallucinations.

![Langflow Architecture](screenshot_canvas.png)

## 🌟 Key Features
- **Multi-Agent Separation of Concerns**: 
  - **Agent 1 (Data Analyst)**: Parses raw historical CSV data and utilizes external computation tools.
  - **Agent 2 (Risk Manager)**: Evaluates the calculated technical metrics against market logic to output executive risk decisions.
- **Function/Tool Calling Integration**: Combines Gemini 1.5 Flash with an external Calculator Tool to eliminate LLM numerical hallucination during volatility math.
- **Context-Aware Parsing**: Handles raw content messages seamlessly from dynamic historical price datasets.

## 🛠️ System Workflow
- **Input**: Historical price dataset (CSV) uploaded by the user along with specific portfolio queries.
- **Process 1**: Agent 1 parses the raw CSV content and triggers the Calculator Tool to execute precise volatility math.
- **Process 2**: Agent 2 ingests the computed metrics and evaluates the overall market risk using custom Prompt Templates.
- **Output**: An executive financial risk report containing structured tactical decisions and checklists.

## 🚀 How to Run
1. Install and run **Langflow** (`pip install langflow`).
2. Create a new flow and select **Upload Project**.
3. Import the `bitcoin-multiagent-risk-analyzer.json` file from this repository.
4. Insert your Gemini API Key in the LLM/Agent configurations.
5. Upload the BTC historical CSV dataset into the **Read File** component and start chatting via **Chat Input**!
