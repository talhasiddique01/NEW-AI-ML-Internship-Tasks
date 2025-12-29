# Auto Tagging Support Tickets Using LLM

## Project Overview
This project demonstrates how to automatically tag support tickets into categories using a Large Language Model (LLM). Support tickets often contain free-text descriptions of user issues, making manual categorization time-consuming and error-prone. This project leverages advanced NLP techniques to classify support tickets efficiently.

---

## Objective
- Automatically assign categories (tags) to support tickets.  
- Compare the performance of **zero-shot** and **fine-tuned** LLMs.  
- Apply **few-shot learning** to improve prediction accuracy.  
- Output the **top 3 most probable tags** for each support ticket.

---

## Dataset
- **Source:** Free-text Support Ticket Dataset  
- **Content:** Unstructured text describing support issues  
- **Format:** CSV file with columns:  
  - `support_ticket_text`: The textual description of the ticket  
  - Other optional metadata columns as available  

---

## Methodology

### 1. Data Preparation
- Load dataset using **pandas**  
- Inspect data for missing values and clean text as necessary  

### 2. LLM-based Tagging
- **Zero-shot learning:**  
  - Directly prompt the LLM to categorize tickets without prior training  
- **Few-shot learning:**  
  - Provide a few labeled examples in the prompt to guide the model  
- **Fine-tuning (optional):**  
  - Train or adapt the LLM on a subset of labeled tickets for better accuracy  

### 3. Output Generation
- Generate **top 3 predicted tags** per ticket  
- Store predictions in a new column in the dataset for analysis  

### 4. Post-processing
- Parse LLM output (if returned as JSON or text) into structured format  
- Optionally, analyze frequent categories  

---

## Skills Gained
- Prompt Engineering  
- LLM-based Text Classification  
- Zero-shot vs Few-shot Learning  
- Multi-class Prediction and Ranking  

---

## Key Results / Observations

- Few-shot learning significantly improved tagging accuracy compared to zero-shot predictions.
- Top 3 tags per ticket allowed better handling of ambiguous tickets.
- JSON-parsed output enabled structured analysis of LLM predictions.
- Frequent categories like Billing Issue, Login Problem, and Technical Issue were clearly identifiable.
- Fine-tuning the model can further enhance performance, particularly for domain-specific issues.
