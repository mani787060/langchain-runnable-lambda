# LangChain RunnableLambda Custom Logic
[![LangChain](https://img.shields.io/badge/Framework-LangChain-green)](https://www.langchain.com/)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![Logic](https://img.shields.io/badge/Concept-Custom%20Logic-orange)](https://python.langchain.com/docs/expression_language/how_to/functions)

## 🏗️ Project Overview
This repository explores **`RunnableLambda`**, the ultimate flexibility tool within the LangChain Expression Language (LCEL). While LangChain offers excellent built-in components, real-world AI engineering constantly requires custom data manipulation. This project demonstrates how to turn any standard Python function into a "Runnable" that can be piped effortlessly between prompts, models, and parsers.

---

## 🛠️ Key Technical Implementations

### 1. The Custom Logic Escape Hatch
* **Function Wrapping:** Converting standard `def` functions or anonymous `lambda` functions into LCEL-compatible components using `@chain` or `RunnableLambda()`.
* **Data Sanitization:** Executing a Python function to scrub personally identifiable information (PII) or reformat strings *before* the data reaches the LLM.

### 2. State Dictionary Management
* **Dictionary Unpacking:** Demonstrating how to write functions that accept the pipeline's dictionary state, extract the necessary keys, compute a result, and return a format the next component expects.
* **Multi-Step Transformations:** Chaining multiple lambdas together to handle complex preprocessing logic without breaking the readability of the `|` syntax.

### 3. Hybrid AI Systems
* **Deterministic Meets Probabilistic:** Blending exact Python logic (e.g., calculating a mathematical score or checking string length) with the creative output of the Gemini Pro model within the same execution sequence.

---

## 💻 Tech Stack
* **Language:** Python 3.9+
* **Orchestration:** LangChain (`langchain-core`, `langchain-google-genai`)
* **Model:** Google Gemini Pro
* **Environment:** `python-dotenv`

---

## 🚀 Getting Started

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/langchain-runnable-lambda-custom-logic.git](https://github.com/your-username/langchain-runnable-lambda-custom-logic.git)

2. **Install Dependencies:**
   ```bash
   pip install -U langchain-core langchain-google-genai python-dotenv

3. **Setup API Key:**
   Create a .env file in the root directory:

   ```bash
   GOOGLE_API_KEY=your_gemini_key_here

4. **Run the Implementation:**
   ```bash
   python runnable_lambda.py   
