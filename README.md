# LoRA Rank Performance Analysis 🔍

## Project Overview 🎯

This project explores the impact of **LoRA (Low-Rank Adaptation)** rank settings on training performance and memory usage. The rank parameter in LoRA plays a crucial role in determining model performance and computational resource utilization. Experiments were conducted with rank values of `[8, 128, 256]` to evaluate:

- Training Loss
- Training Runtime
- CPU and GPU Memory Usage

## Experiment Setup ⚙️

- **Model**: `facebook/opt-350m`
- **Dataset**: `lucasmccabe-lmi/CodeAlpaca-20k`
- **LoRA Rank Values**: `[8, 128, 256]`
- **Evaluation Metrics**:
  - Training Loss
  - Average CPU and GPU Memory Usage
  - Training Runtime

## Results Analysis 📊

### Training Loss
- [View Loss Graph](https://api.wandb.ai/links/wrtyu0603-illinois-institute-of-technology/630d7aty)
- Higher ranks (128 and 256) yielded slightly lower training loss compared to rank 8, indicating more stable learning.  
![Training Loss Graph Placeholder](#)

### Average CPU Memory Usage
- [View CPU Memory Usage Graph](https://api.wandb.ai/links/wrtyu0603-illinois-institute-of-technology/1ocbxayx)
- Rank 8 consumed the least CPU memory, while ranks 128 and 256 had similar usage.  
![CPU Memory Usage Graph Placeholder](#)

### Average GPU Memory Usage
- [View GPU Memory Usage Graph](https://api.wandb.ai/links/wrtyu0603-illinois-institute-of-technology/wyhl2pom)
- GPU memory usage increased with higher ranks, with rank 8 being the most efficient.  
![GPU Memory Usage Graph Placeholder](#)

### Training Runtime
- [View Runtime Graph](https://api.wandb.ai/links/wrtyu0603-illinois-institute-of-technology/m2u59eri)
- Training time increased with higher ranks, with rank 8 being the fastest.  
![Runtime Graph Placeholder](#)

## Conclusion & Summary ✍️

- Higher **LoRA ranks** (128 and 256) required more GPU memory and longer training time but achieved marginally better performance (lower training loss).
- **Rank 8**: Demonstrated the most efficient resource utilization and fastest training, making it suitable for low-resource environments.
- **Rank 256**: Showed slightly improved performance at the cost of higher resource demands, potentially useful for high-performance settings.
