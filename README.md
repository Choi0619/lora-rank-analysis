# 🔍 Comparing Training Performance Based on LoRA Rank

## Project Description 🎯

This project analyzes the impact of **LoRA (Low-Rank Adaptation)** rank adjustments on model performance and memory usage. Rank is one of LoRA's key parameters and affects both model accuracy and resource efficiency. Experiments were conducted with rank values of `[8, 128, 256]` to observe differences in training loss, runtime, and memory usage.

## Experiment Setup ⚙️

- **Model**: `facebook/opt-350m`
- **Dataset**: `lucasmccabe-lmi/CodeAlpaca-20k`
- **Rank Values**: `[8, 128, 256]`
- **Evaluation Metrics**:
  - Training Loss
  - Average CPU and GPU Memory Usage
  - Runtime

## Results Analysis 📊

### Training Loss
- [View Loss Graph](https://api.wandb.ai/links/wrtyu0603-illinois-institute-of-technology/630d7aty)
- Higher ranks demonstrated slightly lower loss values, with **Rank 256 and 128** offering more stable training compared to **Rank 8**.  
![image](https://github.com/user-attachments/assets/22d497ff-820f-4f3a-a7ea-8786e425d0d0)

### Average CPU Memory Usage
- [View CPU Memory Usage Graph](https://api.wandb.ai/links/wrtyu0603-illinois-institute-of-technology/1ocbxayx)
- Rank 8 consumed the least CPU memory, while ranks 128 and 256 showed similar memory usage.  
![image](https://github.com/user-attachments/assets/9d986edb-db66-43d2-ba34-d1c93004be6c)

### Average GPU Memory Usage
- [View GPU Memory Usage Graph](https://api.wandb.ai/links/wrtyu0603-illinois-institute-of-technology/wyhl2pom)
- GPU memory usage increased with higher ranks, with Rank 8 consuming the least memory.  
![image](https://github.com/user-attachments/assets/33b51050-f861-4935-8b91-f3e13d128d53)

### Runtime
- [View Runtime Graph](https://api.wandb.ai/links/wrtyu0603-illinois-institute-of-technology/m2u59eri)
- Higher ranks required longer training times, with Rank 8 demonstrating the fastest runtime.  
![image](https://github.com/user-attachments/assets/09d26c9b-5304-4599-a340-58ff51352011)

## Conclusion and Summary ✍️

- **LoRA Rank**: Increasing the rank results in higher GPU memory consumption and longer runtime but slightly improves training loss.
- **Rank 8**: Demonstrated efficient resource utilization and faster training, making it suitable for **low-resource environments**.
- **Rank 256**: Showed slightly better training performance but required significantly more resources.
