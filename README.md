Model Fine-Tuning and Evaluation with LoRA & Quantization
This repository provides a comprehensive pipeline for loading and fine-tuning a large language model (LLM) using LoRA and quantization for an extractive question-answering task. The process utilizes the transformers and peft libraries, optimized with bitsandbytes quantization, and evaluated on a custom dataset. The model is designed to be fine-tuned on the "Trelis/touch-rugby-rules-memorisation" dataset, focusing on improving model performance for specific rule-based tasks.

Table of Contents
Overview
Prerequisites
Setup & Installation
Training & Fine-Tuning
Evaluation
License
Acknowledgements
Overview
- This project demonstrates how to:
- Set up a runtime environment in Google Colab with high RAM.
- Install necessary libraries and dependencies.
- Load, preprocess, and tokenize data from a custom dataset.
- Load a pre-trained model (OpenChat 3.5) with quantization techniques.
- Apply LoRA for efficient fine-tuning on a specific dataset.
- Evaluate the model's performance using a set of predefined questions.
Key features:

Quantization: Utilizes bitsandbytes to perform model quantization (4-bit, 8-bit) to reduce memory usage and improve performance.
LoRA (Low-Rank Adaptation): Optimizes the model training by reducing the number of trainable parameters.
Evaluation: Provides a question-answering evaluation script to assess the model’s output against predefined answers.
Prerequisites
To run this pipeline, the following dependencies must be installed:

Python 3.7 or higher
torch (with CUDA support)
transformers==4.38.1
peft==0.8.2
bitsandbytes==0.42.0
datasets==2.17.1
scipy==1.12.0
huggingface_hub==0.20.3
wandb==0.16.3
accelerate==0.27.2
Google Colab (for convenience in utilizing GPU/TPU resources)
Additionally, make sure you have access to a high-RAM runtime in Google Colab to handle large model fine-tuning tasks.
