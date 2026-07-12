
[

![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)

](https://colab.research.google.com/drive/1eoXglIrXYLfWVamViu7xwjtg9bRcvoqD?usp=sharing
# Capital_budgeting_AI_chatbot
AI-powered FP&amp;A chatbot that reads a real Excel capital budgeting model and answers financal what-if questions using LLM
# FP&A AI Chatbot — Capital Budgeting Analysis

An AI-powered financial planning & analysis chatbot that reads a real Excel 
capital budgeting model and answers natural language what-if questions using 
a large language model. Built entirely in Python on Google Colab.

---

## Project Overview

This project evaluates the capital investment decision of an Italian 
manufacturing company considering relocating production to Vietnam. The 
chatbot connects directly to a 10-year Excel financial model and allows 
users to ask questions like:

- *"Is this project worth investing in?"*
- *"What happens if we switch to the worst case scenario?"*
- *"How does our IRR compare to the cost of capital?"*
- *"What is the impact of rising interest rates on this project?"*

The chatbot responds with real numbers from the model and analyst-grade 
explanations — not generic AI responses.

---

## Key Features

- Reads live data directly from an Excel capital budgeting model using Python
- Answers natural language financial questions using Llama 3.3 70B via Groq API
- Covers NPV, IRR, WACC, scenario analysis, and sensitivity analysis
- Three-case scenario structure: Best Case, Base Case, Worst Case
- Formats all outputs in clean financial language (€134,087,581 / 15.35% IRR)

---

## Model Outputs (Base Case)

| Metric | Value |
|---|---|
| Net Present Value (NPV) | €134,087,581 |
| Internal Rate of Return (IRR) | 15.35% |
| WACC | ~3.7% |
| IRR vs WACC Spread | +11.6 percentage points |
| Initial Investment | €510,000,000 |
| Senior Debt Facility | €300,000,000 |
| Project Horizon | 10 years |

---

## Excel Model Structure

| Sheet | Description |
|---|---|
| Drivers | All key assumptions and case selection toggle |
| Revenue | 10-year energy production and revenue forecast |
| Opex | Operating expenditure schedule |
| Fixed Asset Roll-Forward | PP&E, Capex, and D&A schedule |
| Financing | Senior debt repayment schedule |
| P&L | Full income statement |
| Cash Flow | Operating and financing cash flows |
| WACC | Cost of equity via CAPM, blended WACC |
| Discounted Cash Flows | NPV, IRR, and sensitivity analysis |

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core programming language |
| Google Colab | Development environment |
| openpyxl | Reading Excel financial model |
| Groq API | LLM inference (Llama 3.3 70B) |
| Llama 3.3 70B | Natural language understanding and response |

---

## How It Works

User Question
↓
Groq API (Llama 3.3 70B) understands the question
↓
Python pulls real numbers from Excel model via openpyxl
↓
LLM generates analyst-grade explanation using model data
↓
Formatted financial answer
---

## Project Structure

fpa-ai-chatbot/
│
├── FPA_Chatbot.ipynb          # Main Colab notebook
├── capital budgeting.xlsx     # Excel financial model
└── README.md                  # Project documentation
---

## Setup Instructions

1. Clone this repository
2. Upload `capital budgeting.xlsx` to your Colab file browser
3. Get a free Groq API key at console.groq.com
4. Open `FPA_Chatbot.ipynb` in Google Colab
5. Run all cells top to bottom
6. Call `fpa_chatbot("your question here")` to interact

---

## Sample Output
===============================
Q: Is this project worth investing in?
A: Based on the model data, the project appears to be worth investing in.
The NPV is €134,087,581, which is positive, indicating the project is
expected to generate value for the company. The IRR of 15.35% is higher
than the WACC of approximately 3.7%, suggesting that the project's returns
are expected to exceed the cost of capital. Overall, the financial metrics
suggest that this project is a viable investment opportunity.
---

## Skills Demonstrated

- Financial modelling (NPV, IRR, WACC, DCF, sensitivity analysis)
- Python programming (openpyxl, API integration, functions, data structures)
- LLM API integration (Groq, prompt engineering, system context design)
- FP&A thinking (scenario analysis, capital budgeting, investment appraisal)
- End-to-end project building from financial model to AI-powered tool

---

## About

Built as a portfolio project to demonstrate applied skills in corporate 
finance, FP&A, and AI tooling — combining Excel financial modelling with 
Python and LLM integration.

*Developed by Prajwal Gowda — BFM Final Year, Guru Nanak Khalsa College, 
Mumbai*
