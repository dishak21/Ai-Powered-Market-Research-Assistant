# 🤖 AI-Powered Market Research Assistant

## 📌 Overview
The **Market Research Assistant** is a multi-model AI system designed to automate the generation of structured, accurate, and verifiable industry reports. Built for the UCL module *Machine Learning for Business (MSIN0231)*, the assistant uses **Wikipedia as the sole source of truth**, ensuring factual grounding and reduced hallucination.

---

## ⚙️ Workflow Architecture

### 🔁 Three-Prompt Pipeline
1. **Generation Prompt**:  
   Claude generates the initial industry report using a strict JSON schema, Wikipedia-only sourcing, and a word limit of 600.

2. **Evaluation Prompt**:  
   GPT-4 evaluates Claude's output using six metrics:
   - Wikipedia Similarity (MiniLM embeddings)
   - Reference Count
   - Hallucinated Facts
   - JSON Validity
   - Structural Completeness
   - Word Count

3. **Refinement Prompt**:  
   Claude receives feedback from GPT-4 and refines the report to resolve issues. The loop continues until strict thresholds are met.

---

## 📐 JSON Report Structure

Each report contains 12 key sections:
1. Industry Overview  
2. Market Analysis  
3. Key Products & Services  
4. Geographical Distribution  
5. Key Players  
6. Regulatory Landscape  
7. Technological Innovations  
8. Market Trends  
9. Opportunities  
10. Challenges  
11. Future Outlook  
12. References  

---

## 📊 Evaluation Metrics

| Metric                  | Description                                           |
|------------------------|-------------------------------------------------------|
| Wikipedia Similarity   | Semantic alignment with Wikipedia (MiniLM)           |
| Reference Count        | Number of valid Wikipedia citations                  |
| Hallucination Count    | Number of fabricated claims                          |
| JSON Validity          | Structural correctness of output                     |
| Structural Completeness| Presence of all required sections                    |
| Word Count             | Must not exceed 600 words                            |

📈 **Overall Score** = Similarity + Reference Count − Hallucinated Facts

---

## 🧪 Models Evaluated

- ✅ **OpenAI GPT-4**: Best accuracy and structure
- ✅ **Anthropic Claude**: Strong second-best for generation & refinement
- ❌ **Google Gemini**: Eliminated due to JSON flaws and high hallucination rates

---

## 🛠 Features

- **Fully automated generation pipeline**
- **Dynamic multi-model collaboration**
- **Quantitative scoring and benchmarking**
- **Hallucination rate reduced from 40% → <5%**
- **Industry-specific model switching**
- **Strict Wikipedia sourcing**

---

## 📝 Sample Industries Covered

- Aerospace & Defence  
- Fashion & Apparel  
- Financial Services  
- Healthcare Technology  
- Renewable Energy

Each report is refined until it meets criteria:
- Similarity ≥ 0.85  
- Reference Count ≥ 1  
- Hallucinated Facts ≤ 1  

---

## 🧱 Limitations & Learnings

### ❌ What Didn't Work
- Single-model prompting led to high hallucination
- Post-generation fact-checking was time-consuming
- Gemini's outputs lacked structural integrity

### ✅ What Worked
- Three-step feedback loop between Claude and GPT-4
- Wikipedia-based similarity scoring
- Iterative refinement until quality met

---

## 🚀 Future Enhancements

- Integrate financial APIs (e.g. Yahoo Finance, Bloomberg)
- Add web scraping for corporate filings
- Use ML-based refinement learning from past feedback
- Enable AWS/Azure cloud scaling for batch report generation
- Implement RBAC and GDPR compliance for enterprise use

---

## 📚 Source of Truth

All facts are **strictly sourced from Wikipedia**. The system rejects unverifiable content, ensuring high factual integrity and replicability across use cases.

---

## 📂 File Outputs

Reports are delivered in:
- Structured JSON (machine-readable)
- Markdown/PDF for presentation
- Logs of evaluation scores for each model

---

## 💬 Contact

*Let’s connect if you're interested in scalable, trustworthy AI for industry insights.*
