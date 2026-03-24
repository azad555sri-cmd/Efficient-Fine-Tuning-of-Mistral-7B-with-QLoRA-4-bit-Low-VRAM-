Efficient Fine-Tuning of Mistral-7B with QLoRA (4-bit, Low VRAM)

This repository demonstrates parameter-efficient fine-tuning of the Mistral-7B language model using QLoRA and 4-bit quantization. It’s optimized for low GPU memory setups, enabling large language model fine-tuning on consumer hardware. The model is fine-tuned on the IMDb dataset for sentiment analysis.

Features
 - 4-bit quantization with BitsAndBytes for VRAM efficiency
 - LoRA (Low-Rank Adaptation) for parameter-efficient fine-tuning
 - Hugging Face Trainer integration for easy training
 - Supports GPU and CPU offloading automatically
 - Tokenization and dataset preprocessing included

The usage of your project is essentially efficiently fine-tuning a large language model (LLM) on a specific task while using minimal GPU resources. More concretely:

Primary Purpose
1 Fine-tune Mistral-7B for downstream tasks
   - In your code, you used the IMDb dataset for sentiment analysis, but the setup can work for any text-based task (e.g., classification, summarization, question answering).
2 Use parameter-efficient techniques (QLoRA + 4-bit quantization)
   - Instead of retraining all 7 billion parameters (which is expensive), LoRA allows you to train only a small subset of parameters, saving memory and compute.
   - 4-bit quantization reduces model memory footprint so it can fit on consumer GPUs (8–12GB VRAM) instead of massive server GPUs.
3 Demonstrate practical LLM training on limited hardware
   - This makes the project valuable for people who want to experiment with large models without access to huge GPU clusters.

