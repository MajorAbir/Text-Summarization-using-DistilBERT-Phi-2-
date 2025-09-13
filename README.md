# Text-Summarization-using-DistilBERT-Phi-2

This repository presents a **hybrid Transformer-based summarization model** that combines the lightweight efficiency of **DistilBERT** (encoder) with the powerful generative capabilities of **Phi-2** (decoder). The model is designed for high-quality **abstractive summarization**, especially across domains such as **legal, academic, business, and news** documents.

---

## 🚀 Features

- ⚡ **DistilBERT Encoder**: Efficient token encoding with reduced computation.
- 🧠 **Phi-2 Decoder**: Transformer-based causal language model for fluent summary generation.
- 📊 **ROUGE Evaluation**: Built-in ROUGE-1, ROUGE-2, and ROUGE-L metric computation with accuracy tracking.
- 📉 **Memory-Efficient**: Optimized for FP16 (half-precision) inference & training on Google Colab.
- 📦 Easy-to-use interface for both training and inference.

---


---

## 🔧 Installation

Install required dependencies:

```bash
pip install transformers
pip install evaluate
pip install datasets  # optional
```

---

## 🧪 Example Inference

```python
sample_text = "The stock market saw a significant rise today due to increasing investor confidence."
summary = generate_summary(sample_text)
print("Generated Summary:", summary)
```

---

## 📈 ROUGE Evaluation

The model supports ROUGE-based evaluation:

```python
reference = ["Investor confidence caused a significant rise in the stock market today."]
generated = [summary]
evaluate_rouge(reference, generated)
```

Example Output:

```
--- ROUGE Evaluation ---
ROUGE-1: 0.4390
ROUGE-2: 0.2564
ROUGE-L: 0.3415
```

---

## 📊 Visualizations

![ROUGE Bar Graph](outputs/rouge_score_evaluation.png)

---

## 🏗️ Model Architecture

![Model Architecture](./Text%20Summarization%20using%20DistilBERT-Phi%202%20Arch%20Diagram.png)


---

## 🎯 Future Work

- Fine-tune Phi-2 specifically for summarization tasks.
- Add RLHF (Reinforcement Learning with Human Feedback).
- Extend support for longer documents (via LongRoPE).
- Build a lightweight API for real-time summarization.

---


## 🙌 Acknowledgements

- [Hugging Face Transformers](https://huggingface.co/)
- [Microsoft Phi-2](https://huggingface.co/microsoft/phi-2)
- [ROUGE Evaluation Library](https://github.com/huggingface/evaluate)
