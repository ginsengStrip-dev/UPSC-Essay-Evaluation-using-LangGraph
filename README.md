# UPSC Essay Evaluation using LangGraph

A **parallel LLM-based workflow** built with **LangGraph** to evaluate UPSC essays across multiple dimensions and provide structured, summarized feedback.

---

## Features

- **Language Quality** – Evaluates grammar, vocabulary, and coherence.
- **Clarity of Thought** – Assesses logical flow and organization of ideas.
- **Depth of Analysis** – Measures critical thinking, insight, and argument strength.

All evaluations are performed **in parallel**, and results are aggregated to provide a **summarized overall feedback** along with an **average score**.

---

## Tech Stack

- **Python**  
- **LangGraph**  
- **LLM API**  
- **TypedDicts** for structured input/output data  

---

## Highlights

- **Parallel Execution:** Multiple evaluation nodes run simultaneously for efficiency.  
- **Structured & Typed Data:** Uses `TypedDict` for clean, clear input/output.  
- **Modular & Scalable:** Easy to extend to new evaluation metrics or additional workflows.  

---

## Example Usage

```python
initial_state = {
    'essay': "Your essay text here..."
}

final_state = workflow.invoke(initial_state)
print(final_state['overall_feedback'])
print(final_state['average_score'])
