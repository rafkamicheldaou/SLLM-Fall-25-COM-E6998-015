# Week 4 – Scaling Transformers for Long Context

This week focuses on **techniques and architectures that extend the scalability of Transformers**, enabling them to handle extremely long sequences efficiently. These works explore theoretical foundations, memory-efficient designs, and fine-tuning methods to push context lengths to 100k tokens and beyond.

---

##  Papers

### 1. [Transformers are SSMs: Generalized Models and Efficient Algorithms Through Structured State Space Duality (SSD)](https://arxiv.org/abs/2405.21060)
**Authors:** Tri Dao, Albert Gu (2024)  
- Introduces a **theoretical bridge between Transformers and State Space Models (SSMs)**, showing that attention mechanisms and SSMs are deeply connected through **structured semiseparable matrices**.  
- Proposes **Mamba-2**, an architecture that is **2–8× faster** than Mamba while matching or outperforming Transformers on language modeling tasks.  
- Key contribution: the **Structured State Space Duality (SSD)** framework, which allows transferring optimization techniques from Transformers to SSMs for both speed and scalability.

---

### 2. [LongLoRA: Efficient Fine-Tuning of Long-Context Large Language Models](https://arxiv.org/abs/2309.12307) 
**Authors:** Yukang Chen, Shengju Qian, Haotian Tang, Xin Lai, Zhijian Liu, Song Han, Jiaya Jia (ICLR 2024)  
- Presents **LongLoRA**, a lightweight fine-tuning strategy that extends an LLM’s context window (e.g., Llama2 7B from **4k → 100k tokens**) on a **single 8×A100 machine**.  
- Combines:
  - **S2-Attn (Shifted Sparse Attention):** approximates long attention during training with sparse local attention for computational savings.
  - **Improved LoRA:** trains embeddings and normalization layers to better adapt to longer contexts.
- Compatible with **FlashAttention-2** and other optimization libraries, enabling cost-effective context extension.

---

### 3. [Ring Attention with Blockwise Transformers for Near-Infinite Context](https://arxiv.org/abs/2310.01889)
**Authors:** Hao Liu, Matei Zaharia, Pieter Abbeel (2023)  
- Solves the **memory bottleneck of Transformers** by distributing long sequences across multiple devices in a **ring topology**.  
- Overlaps **key-value block communication** with blockwise attention computation, achieving **zero additional communication overhead**.  
- Enables training and inference with **millions of tokens** in context length, scaling **linearly with the number of devices** without approximations.

---

### 4. [FlashAttention-2: Faster Attention with Better Parallelism and Work Partitioning](https://arxiv.org/abs/2307.08691)
**Author:** Tri Dao (2023)  
- Improves on the original **FlashAttention** algorithm with better GPU **work partitioning and parallelism**, reaching **50–73% of theoretical max FLOPs/s**.  
- Provides **2× speedup** over FlashAttention and **up to 10–20× memory savings**, making it essential for training models with long sequence lengths (e.g., GPT-4, Claude, MPT).  
- Widely adopted in production systems and compatible with methods like **LongLoRA**.

---

## Summary
- **SSD & Mamba-2:** Unifies Transformers and SSMs, offering faster alternatives to standard attention.
- **LongLoRA:** Practical fine-tuning approach to expand context windows for pre-trained models.
- **Ring Attention:** Achieves near-infinite context scaling with multi-device communication strategies.
- **FlashAttention-2:** Provides the core memory and speed optimizations that power long-context models.

Together, these papers showcase the **state-of-the-art methods for scaling LLMs** to handle unprecedented context lengths efficiently.


