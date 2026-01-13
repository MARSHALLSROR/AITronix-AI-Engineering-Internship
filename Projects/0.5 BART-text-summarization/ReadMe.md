# BART Text Summarization — BBC News

## Overview
This project demonstrates **abstractive text summarization** using a pretrained **BART encoder–decoder transformer** from Hugging Face.

The objective is to show how modern transformer models can be used for **text generation tasks** beyond classification, using real-world news articles as input.

This work extends a previous project on **BBC News text classification with BERT**, highlighting the transition from **encoder-only models** to **encoder–decoder architectures**.

---

## Model
- **Model:** facebook/bart-large-cnn  
- **Architecture:** Encoder–Decoder Transformer  
- **Framework:** PyTorch + Hugging Face Transformers  
- **Mode:** Inference only (no fine-tuning)

BART is well-suited for long-form news summarization and generates summaries that paraphrase the original text rather than extracting sentences verbatim.

---

## Dataset
- **Source:** BBC News Dataset (Kaggle)
- **Usage:** Text input only

The dataset is used purely as a source of raw news articles for summarization.  
No labels, training, or evaluation splits are required for this task.

---

## Methodology
1. Raw news articles are lightly cleaned (whitespace normalization only).
2. Text is tokenized using the BART tokenizer.
3. The pretrained BART model generates summaries using beam search.
4. Output token IDs are decoded into human-readable text.

---

## Example Output

**Original Article (excerpt):**
> The government has announced new measures aimed at stabilizing the economy following recent market volatility...

**Generated Summary:**
> The government introduced new economic measures in response to market instability, aiming to restore confidence and support long-term growth.

## Key Concepts Demonstrated
- Encoder vs encoder–decoder transformers
- Abstractive text generation
- Token length limits and truncation
- Inference with pretrained NLP models
- Practical use of Hugging Face Transformers

---

## Demo
A short demo video showing live summarization output was recorded and shared on LinkedIn.

---

## Notes
- Model weights are not included in this repository.
- The notebook is fully reproducible and downloads pretrained weights automatically via Hugging Face.
