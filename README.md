📊 AI-Powered Market Research Assistant
Overview
This project presents a robust AI-based pipeline for automated industry report generation, designed to meet high standards of factual accuracy, structural integrity, and consistency. The system leverages multiple large language models (LLMs) in a multi-prompt, multi-model workflow to produce reports that adhere strictly to Wikipedia-sourced information.

🔧 How It Works
⚙️ Multi-Prompt Pipeline
The assistant follows a three-stage prompt structure:

Generation Prompt:
Claude (or other LLMs) generates a report based on predefined JSON structure and Wikipedia sourcing rules.

Evaluation Prompt:
OpenAI (GPT-4) acts as a quality control evaluator, reviewing the output on six key metrics:

Wikipedia Similarity (0–1)

Number of Wikipedia References

Count of Hallucinated Facts

Valid JSON Structure (Yes/No)

Structural Consistency (Yes/No)

Word Count

Refinement Prompt:
Claude receives the evaluation results and is prompted to refine the report, resolving all flagged issues.

This cycle repeats until the report meets defined thresholds (e.g., ≥0.85 similarity, ≤1 hallucination).

🧠 Model Roles
Claude:
Generates and refines the initial report.

OpenAI GPT-4:
Critically evaluates outputs for factual and structural accuracy.

This division of labor creates a high-performing pipeline where no single model is relied on for everything.

📈 Evaluation Strategy
Each model is benchmarked across multiple industries (e.g., Energy, Fashion, Finance, Healthcare, Aerospace) using objective and reproducible metrics:

Validity (JSON parsability)

Completeness (all 12 sections present)

Semantic similarity to Wikipedia

Citation quality

Hallucination detection

Based on these, OpenAI consistently performed best, with Claude as the runner-up. Gemini was eliminated due to structural and factual issues.

🔬 Key Innovations
Dynamic Model Collaboration: Each model’s strengths are used strategically.

Quantitative Evaluation Framework: Six concrete metrics for ranking model outputs.

Automated Refinement Loop: Refinement based on structured JSON feedback.

Wikipedia-Based Ground Truth: Reduces hallucination rate from 40% → under 5%.

🧪 Sample Use Cases
Competitive intelligence and industry benchmarking

Rapid internal briefings and executive summaries

Automated report generation for sales, product, or market teams

🛠 Future Enhancements
Integrate financial APIs (e.g., Yahoo Finance, Bloomberg) for richer insights

Add live scraping of filings and reports

Use ML-based refinement to reduce iteration cycles

Enable multi-threaded cloud deployment (AWS/Azure)

Implement RBAC and encryption for enterprise-grade security

📁 Output Format
Each report follows a 12-section JSON schema, including:

Industry Overview

Market Size & Growth

Key Players

Regulatory Landscape

Market Trends

Future Outlook
...and more.

📚 Source of Truth
All factual claims are backed by Wikipedia. Reports must cite Wikipedia and structurally align with verified data — ensuring high factual integrity and reproducibility.

