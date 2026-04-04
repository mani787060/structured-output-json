# Gemini Structured Output with JSON Schema
[![JSON](https://img.shields.io/badge/Format-JSON%20Schema-blue)](https://json-schema.org/)
[![LangChain](https://img.shields.io/badge/Framework-LangChain-green)](https://www.langchain.com/)
[![Google AI](https://img.shields.io/badge/Model-Gemini%20Pro-4285F4)](https://ai.google.dev/)

## 🏗️ Project Overview
This repository demonstrates how to extract **Structured Data** from Google Gemini using raw **JSON Schemas**. While Python-specific tools like Pydantic are convenient, using raw JSON Schema is the industry standard for building interoperable AI systems. This project showcases how to define a universal data contract that ensures the LLM returns perfectly formatted JSON, ready for consumption by any frontend or backend service.

---

## 🛠️ Key Technical Implementations

### 1. Universal Schema Definition
* **JSON Schema Standards:** Using standard keys like `type`, `properties`, and `required` to define the data structure.
* **Constraint Enforcement:** Utilizing `enum` to restrict AI responses to specific categories and `description` to provide semantic guidance to the model.

### 2. LangChain Integration
* **`.with_structured_output()`:** Passing a raw Python dictionary representing the JSON schema directly into the LangChain engine.
* **Native Parsing:** Leveraging Gemini's internal tool-calling capabilities to ensure the response adheres strictly to the provided JSON blueprint.

### 3. Interoperability & Scalability
* **Language Agnostic:** Demonstrating a workflow that can be shared across different tech stacks (Web, Mobile, Backend).
* **Zero Dependency:** Showing how to achieve structured outputs without relying on Pydantic-specific features.

---

## 💻 Tech Stack
* **Language:** Python 3.9+
* **Orchestration:** LangChain (`langchain-core`, `langchain-google-genai`)
* **Core Logic:** JSON Schema (Dictionary-based)
* **Model:** Google Gemini Pro
* **Environment:** `python-dotenv`

