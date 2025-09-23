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
See [papers.md](./papers.md) for this week's papers and reading materials.
