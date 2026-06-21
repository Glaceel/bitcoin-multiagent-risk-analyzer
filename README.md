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

## 📊 Dataset Structure
The system expects a historical price dataset in CSV format with the following structure (you can find a sample file in `dataset_sample.csv`):
```csv
Date,Open,High,Low,Close,Volume
2025-10-10,61000,62500,60800,62200,1500000000
2025-11-25,58000,59000,53500,54000,3200000000
