# 📰 BBC News Text Classification with BERT

## Project Overview

This repository contains a **transformer-based NLP project** that performs **multi-class text classification** on BBC News articles using a **fine-tuned BERT model**.

The focus of this repository is on:

- Correct use of modern NLP pipelines  
- Clean, readable code and notebooks  
- Clear visualization and evaluation of results  

Large trained model files are intentionally excluded to keep the repository lightweight and GitHub-friendly.

---

## Problem Statement

### Task

Classify a news article into one of **five categories**:

- Business  
- Entertainment  
- Politics  
- Sport  
- Tech  

**Type:** Multi-class text classification

---

## Dataset

- **Source:** BBC News Dataset (Kaggle)  
- **Total samples:** ~2,200 articles  
- **Classes:** 5  
- **Split:** 80% training / 20% testing (stratified)  

The dataset is clean and well-structured, making it suitable for controlled model comparison.

---

## Approach

### Preprocessing

Minimal text cleaning was applied:

- Lowercasing  
- Removing non-text symbols  
- Normalizing whitespace  

No stopword removal or stemming was used, as this is **BERT-friendly preprocessing**.

---

### Tokenization

- **Tokenizer:** `bert-base-uncased`  
- WordPiece subword tokenization  
- Outputs:
  - `input_ids`
  - `attention_mask`
- Maximum sequence length: **512 tokens**

---

### Model

- **Architecture:** `BertForSequenceClassification`  
- **Base model:** `bert-base-uncased`  
- **Number of labels:** 5  
- **Training strategy:** Fine-tuning (no training from scratch)

---

## Training Setup

- **Framework:** PyTorch + Hugging Face Transformers  
- **Epochs:** 3  
- **Batch size:** 8  
- **Optimizer:** AdamW  
- **Learning rate:** 2e-5  
- **Scheduler:** Linear decay  
- **Device:** GPU (Kaggle)  

The model converges quickly due to transfer learning, with optimal performance achieved within **2–3 epochs**.

---

## Evaluation Results

### Quantitative Performance

- **Test Accuracy:** ~98%  
- **Macro F1-score:** ~0.98  
- **Weighted F1-score:** ~0.98  

Performance is consistent and balanced across all classes.

---

### Visualizations

This repository includes generated evaluation visuals such as:

- Confusion Matrix  
- Per-class F1-score plots  

These visualizations help interpret model behavior and error patterns.

---

## Model Comparison

| Model | Accuracy |
|------|----------|
| TF-IDF + SVM | ~98–99% |
| Bi-LSTM | ~95–96% |
| **BERT (this project)** | **~98%** |

While classical models perform strongly on this clean dataset, BERT provides superior **contextual and semantic understanding**, with better generalization potential.

---

## Repository Contents

Included:

- Jupyter notebooks with full implementation  
- Evaluation plots and result images  
- Documentation explaining the approach and findings  

Excluded:

- Trained model binaries (due to GitHub file size limits)

---

## Model Artifacts

Trained model files (e.g. `pytorch_model.bin`) are **not included** in this repository due to GitHub’s 100 MB file size limit.

The model was saved using Hugging Face’s standard format during training and can be:

- Reproduced by rerunning the notebook  
- Accessed via the Kaggle notebook output if needed  

---

## Key Takeaways

- Transformer models converge quickly when fine-tuned on small, clean datasets  
- Increasing epochs does not necessarily improve performance  
- BERT’s strength lies in **semantic representation**, not just raw accuracy  
- Proper evaluation and visualization are essential for trustworthy results  

---

## Next Steps

- Extend transformer usage beyond classification  
- Apply encoder–decoder models for **text summarization**  
- Explore generalization on larger or noisier datasets  

---

## Conclusion

This project demonstrates a **complete and well-structured transformer-based NLP workflow**, covering:

- Data preparation  
- Fine-tuning  
- Evaluation  
- Interpretation  

The emphasis is on **correct methodology**, not just performance metrics.
