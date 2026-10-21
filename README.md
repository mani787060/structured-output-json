# Structured Output with JSON Schema

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![JSON Schema](https://img.shields.io/badge/Schema-JSON%20Schema-blue)](https://json-schema.org/)
[![LangChain](https://img.shields.io/badge/Framework-LangChain-green)](https://www.langchain.com/)
[![Google Gemini](https://img.shields.io/badge/LLM-Google%20Gemini-4285F4)](https://ai.google.dev/)

## 📌 Project Overview

This project explores how **JSON Schema can define structured outputs for Large Language Models (LLMs)** in Generative AI applications.

LLMs often generate responses in natural language, which can be difficult to process reliably in software applications. JSON Schema provides a standardized way to describe the expected structure of data, including its properties, data types, required fields, and permitted values.

When integrated with LangChain and a compatible Google Gemini model, a schema can guide the model toward producing structured information that is easier to consume in downstream applications.

## 🎯 Learning Objectives

- Understand JSON Schema and its role in structured data generation.
- Define expected output fields and data types.
- Use constraints such as `required` and `enum`.
- Explore structured output generation with LangChain.
- Understand why structured responses still need appropriate validation and error handling.

## 🛠️ Key Concepts

### 1. JSON Schema Definition

JSON Schema describes the expected structure of a JSON object.

For example:

```python
review_schema = {
    "title": "Review",
    "type": "object",
    "properties": {
        "summary": {
            "type": "string",
            "description": "A brief summary of the review."
        },
        "sentiment": {
            "type": "string",
            "enum": ["positive", "negative", "neutral"]
        }
    },
    "required": ["summary", "sentiment"]
}
```

This schema describes a review object containing a summary and a sentiment selected from three permitted values.

### 2. LangChain Integration

LangChain provides structured output interfaces that can connect a supported chat model to a defined schema.

Using `with_structured_output()` with a compatible model and schema can simplify the process of obtaining structured results without manually extracting JSON from free-form text.

The exact supported schema formats and output behavior depend on the model integration and its capabilities.

### 3. Constraints and Reliability

Schema fields help communicate the expected response structure. Constraints such as `required`, `enum`, and data types can reduce formatting inconsistencies.

However, applications should still handle model errors, missing or unexpected values, and failed requests appropriately. Structured output does not automatically guarantee that every generated value is factually correct.

### 4. Interoperability

JSON is widely supported across programming languages and application environments. A consistent schema can make it easier to transfer structured data between Python services, APIs, frontends, and databases.

## 🧰 Tech Stack

- **Language:** Python
- **LLM Framework:** LangChain
- **Model Provider:** Google Gemini
- **Data Format:** JSON
- **Schema Standard:** JSON Schema
- **Environment Configuration:** `python-dotenv` (if used in the implementation)

## 🚀 Getting Started

### Prerequisites

- Python installed on your system
- Required project dependencies
- A Google Gemini API key if the application calls Gemini

### Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/mani787060/structured-output-json.git
   ```

2. Navigate to the project directory:

   ```bash
   cd structured-output-json
   ```

3. Install the dependencies listed in your project’s `requirements.txt`:

   ```bash
   pip install -r requirements.txt
   ```

4. Configure your API key using the environment variable expected by your Python file. If the implementation uses `python-dotenv`, store the key in a local `.env` file and do not commit that file.

5. Run the Python script using its actual filename:

   ```bash
   python app.py
   ```

   Replace `app.py` with the filename in your repository if it differs.

## 📚 Key Takeaways

JSON Schema provides a standardized contract for describing structured data. Combined with a compatible LLM and LangChain, it can make AI outputs easier to integrate into applications. Reliable systems should also include appropriate error handling, validation, and checks for semantic correctness.

## 👨‍💻 Author

**Mani Ratan**

- GitHub: [@mani787060](https://github.com/mani787060)
- Repository: [structured-output-json](https://github.com/mani787060/structured-output-json)
