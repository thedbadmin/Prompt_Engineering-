
# 📌 Prompt Library – Usage Guide

This repository contains a curated set of **prompt templates** for AI tools like **ChatGPT**, **Claude**, and other LLM-based assistants.  
It also provides guidelines for managing API keys securely using `.env` files.

---

## 🚀 How to Use Prompt `.md` Files

Each prompt is stored as a **Markdown (`.md`) file** under the `prompts/` folder.

### 1️⃣ Copy & Paste into AI Tools

1. Open the `.md` file of interest (e.g., `debugging_prompt.md`).  
2. Copy the **template code block**.  
3. Paste it directly into your AI tool's chat interface (ChatGPT, Claude, or any LLM console).  
4. Replace placeholders such as `[project]`, `[stack trace]`, `[goal]` with your specific details.

Example:
```
Problem context: My ASP.NET app, Equinox project
Error message: System.NullReferenceException in Program.cs
What I tried: Re-seeded DB, restarted app
Expected behavior: DB should initialize with sample classes
Give 3 hypotheses ranked by likelihood + test steps.
```

---

### 2️⃣ Best Practices for Modifying Placeholders

- **Keep context clear:** Always provide:
  - *Project name or environment*  
  - *Exact error message or input data*  
  - *Expected outcome or goal*  
- **Be explicit:** Instead of "fix my code," specify:
  - "Show 3 root causes and test steps for this DB error."  
- **Avoid vague terms:** Replace "this thing" with actual file names, functions, or logs.  
- **Reuse patterns:** Store good custom prompts in a personal `.md` file for later reuse.

---

## 🔑 Using API Keys Securely with `.env` Files

When working with LLMs programmatically (Python, Node.js, etc.), you should **never hardcode your API keys** in your code.

### 1️⃣ Create a `.env` File

In your project folder, create a file named `.env`:

```
OPENAI_API_KEY=your_openai_api_key_here
ANTHROPIC_API_KEY=your_claude_api_key_here
```

*(Do not wrap values in quotes)*

---

### 2️⃣ Load the `.env` in Your Code

#### Python Example (`dotenv` package)
```python
from dotenv import load_dotenv
import os

load_dotenv()

api_key = os.getenv("OPENAI_API_KEY")
print("Using API Key:", api_key)
```

#### Node.js Example (`dotenv` package)
```javascript
require('dotenv').config();

const apiKey = process.env.OPENAI_API_KEY;
console.log("Using API Key:", apiKey);
```

---

### 3️⃣ Add `.env` to `.gitignore`

Never commit `.env` files to GitHub.  
Create or update `.gitignore`:
```
.env
```

This prevents accidental leaks of sensitive credentials.

---

## ✅ Summary

- Use `.md` prompts as **copy-ready templates**.  
- Replace placeholders with specific context for better AI results.  
- Store API keys in `.env` (never in code or repos).  
- Share or fork this repo safely – it’s prompt-only, no secrets included.

---

Happy prompting! 🚀

