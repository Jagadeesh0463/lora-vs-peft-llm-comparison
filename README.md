# lora-vs-peft-llm-comparison-
Public Comparative analysis of LoRA and PEFT techniques across top LLMs.
# 📊 LoRA & PEFT — AI Model Analysis

This project analyzes which major AI models support **LoRA (Low-Rank Adaptation)** and **PEFT (Parameter-Efficient Fine-Tuning)**, and why some models do not.

---

## 🧠 Key Summary

### ✅ Models Supporting LoRA & PEFT

* LLaMA (Meta)
* Mistral / Mixtral
* Qwen (Alibaba)
* DeepSeek
* Phi (Microsoft)
* Falcon

**Reason:**
These are **open-weight models**, allowing direct access to parameters required for LoRA/PEFT.

---

### ⚠️ Partial / Limited Support

* Gemma (Google DeepMind) → Works, but weaker performance
* Gemini → Only via server (not user-accessible)

**Reason:**
Either **performance limitations** (Gemma) or **controlled infrastructure** (Gemini via Vertex AI).

---

### ❌ Models NOT Supporting LoRA & PEFT

* GPT-4.x (OpenAI)
* Claude (Anthropic)

**Reason:**
These are **closed-weight models**:

* No access to internal weights
* Fine-tuning is restricted to APIs (SFT, RLHF, etc.)
* Safety and business constraints

---

## 🔑 Core Insight

LoRA/PEFT depend on **weight access**, not model architecture.

* Open weights → Supported
* Closed weights → Not possible

---

## 📌 Conclusion

* Use **LLaMA / Mistral / Qwen** for full control and experimentation
* Use **GPT / Claude / Gemini** for managed, production-grade APIs
