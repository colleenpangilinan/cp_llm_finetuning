LLM Fine-Tuning with Transformers
Full fine-tuning of Qwen/Qwen2.5-0.5B-Instruct on a multiple-choice question dataset using Hugging Face Transformers and TRL. Measures accuracy before and after training to quantify improvement and check for catastrophic forgetting.

What's covered

Loaded and formatted MCQ data into chat-style training examples (user: question + options / assistant: \boxed{answer})
Used MMLU (machine_learning subset) as additional training data for better generalization
Established a zero-shot baseline before any fine-tuning
Fine-tuned with TRL's SFTTrainer — AdamW-8bit optimizer, cosine LR schedule, cross-entropy loss over answer tokens
Re-evaluated post-training on the same held-out MCQ set to measure accuracy improvement
Ran inference on a held-out test set and saved predictions to CSV


Stack
Python, PyTorch, Hugging Face transformers, datasets, trl, bitsandbytes
Models
Qwen/Qwen2.5-0.5B-Instruct — 0.5B parameter transformer-based causal language model
