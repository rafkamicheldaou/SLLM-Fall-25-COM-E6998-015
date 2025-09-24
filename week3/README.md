# Week 3: Training at Scale (Parallelism & Scheduling)

**Module I: Foundations**

This week introduces students to the foundations of **training large-scale models**, with a focus on scaling laws, distributed training, and the core building blocks of efficient inference.  
Students will explore how empirical discoveries such as **Scaling Laws** (Kaplan et al., 2020) and **Chinchilla** (Hoffmann et al., 2022) shaped our understanding of **data–compute–model tradeoffs**.  

We also cover modern **distributed training systems** such as **Megatron-LM**, **Alpa**, and **ZeRO++**, and examine mechanisms behind **attention**, **KV caching**, and newer **selective state-space models** like **Mamba** and **Bamba**.

---

## Learning Outcomes
By the end of this week, students will be able to:

- **Explain** scaling laws and their implications for model size, dataset size, and compute budgets.
- **Compare** different distributed training strategies, including data, model, and pipeline parallelism.
- **Understand** attention mechanisms, KV caching, and state-space models as building blocks for **efficient inference scaling**.

---

## Key Topics
- Scaling Laws: *Kaplan et al. (2020), Hoffmann et al. (2022)*
- Distributed Training Systems: *Megatron-LM, Alpa, ZeRO++*
- Parallelism Strategies: Data, Model, Pipeline, and FSDP
- Attention and KV Caching
- State-Space Models (Mamba, Bamba)

---

## Resources
- [NVIDIA Megatron-Core User Guide](https://docs.nvidia.com/megatron-core/developer-guide/latest/user-guide/index.html)
- [AllenInstitute/distributed-vae (GitHub)](https://github.com/AllenInstitute/distributed-vae)

---
## Papers
See [papers](./papers) for this week's papers and reading materials.

---

### 1. Megatron-LM
**Title:** Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism  
**Authors:** Mohammad Shoeybi, Mostofa Patwary, Raul Puri, Patrick LeGresley, Jared Casper, Bryan Catanzaro  
**Link:** [arXiv:1909.08053](https://arxiv.org/abs/1909.08053)  
**File:** [View PDF](https://drive.google.com/file/d/MegatronFileID/view?usp=sharing)

---

### 2. ZeRO
**Title:** ZeRO: Memory Optimizations Toward Training Trillion Parameter Models  
**Authors:** Samyam Rajbhandari, Jeff Rasley, Olatunji Ruwase, Yuxiong He  
**Link:** [arXiv:1910.02054](https://arxiv.org/abs/1910.02054)  
**File:** [View PDF](https://drive.google.com/file/d/ZeroFileID/view?usp=sharing)

---

### 3. Alpa
**Title:** Alpa: Automating Inter- and Intra-Operator Parallelism for Distributed Deep Learning  
**Authors:** Lianmin Zheng, Zhuohan Li, Hao Zhang, Yonghao Zhuang, Zhifeng Chen, Yanping Huang, Yida Wang, Yuanzhong Xu, Danyang Zhuo, Eric P. Xing, Joseph E. Gonzalez, Ion Stoica  
**Link:** [arXiv:2201.12023](https://arxiv.org/abs/2201.12023)  
**File:** [View PDF](https://drive.google.com/file/d/AlpaFileID/view?usp=sharing)

---

### 4. ZeRO++
**Title:** ZeRO++: Extremely Efficient Collective Communication for Giant Model Training  
**Authors:** Guanhua Wang, Heyang Qin, Sam Ade Jacobs, Connor Holmes, Samyam Rajbhandari, Olatunji Ruwase, Feng Yan, Lei Yang, Yuxiong He  
**Link:** [arXiv:2306.10209](https://arxiv.org/abs/2306.10209)  
**File:** [View PDF](https://drive.google.com/file/d/ZeroPlusPlusFileID/view?usp=sharing)
