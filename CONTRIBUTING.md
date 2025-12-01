# Contributing to Snip EMR Assistant

First off, thank you for your interest in improving **Snip EMR Assistant – WinRT OCR + Linguistic Cleanup + Local LLM + Deep Disease Scanner**.

This document explains how to contribute safely and productively, with a special focus on:

- Protecting patient privacy,
- Improving robustness of the **Deep Disease Scanner**,
- Keeping the project clearly **pre-regulatory / research-grade**.

---

## 1. Code of Conduct

By participating in this project, you agree to:

- Be respectful and constructive.
- Avoid sharing sensitive or identifiable medical information.
- Help maintain a culture of **safety**, **transparency**, and **honesty about limitations**.

If you see behavior that violates these principles, please raise it via the issue tracker.

---

## 2. Important Safety & Privacy Rules

### ✅ Absolutely do:

- Use **synthetic** or **anonymized** text when creating examples and tests.
- Focus on:
  - Code quality and architecture.
  - OCR robustness and error handling.
  - Disease-scanner **precision/recall** improvements, with tests.
  - Better prompts and output formatting.

### ❌ Never do:

- Upload or paste any **Protected Health Information (PHI)** or identifiable patient data.
- Use real patient documents in GitHub issues, PRs, or discussions.
- Make new UI text or documentation that claims:
  - “Diagnosis”,
  - “Automated risk scoring”,
  - “Clinical decision support”,
  - Or any language implying the tool alone is sufficient for clinical decisions.

Remember: **this is not a medical device**, and we want to keep the open-source repo clearly positioned as **research/assistant tooling**.

---

## 3. How to Propose Changes

1. **Open an Issue** (recommended)
   - Describe the bug, enhancement, or clinical-logic concern.
   - Include **non-PHI** sample text if relevant, e.g.:
     ```text
     SAMPLE NOTE (synthetic):

     PMH: Hypertension, diabetes type 2, CKD stage 3. No history of CAD.
     ```
   - For disease-scanner bugs, specify whether it’s a:
     - False positive (scanner flagged disease but note says no),
     - False negative (disease present but not flagged),
     - Misclassification (e.g., family history vs active problem).

2. **Fork the Repository**

3. **Create a Feature Branch**
   ```bash
   git checkout -b feature/improve-cad-regex
