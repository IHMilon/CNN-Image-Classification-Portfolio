# MobileNetV2 on PlantVillage Dataset

## Overview
This project implements a **custom MobileNetV2-style CNN** from scratch in PyTorch for **PlantVillage image classification**.  
The model is optimized for **high accuracy**, **low computational cost**, and **minimal parameters**, making it suitable for edge deployment.
## References
- MobileNetV2 Paper: [MobileNetV2: Inverted Residuals and Linear Bottlenecks](https://arxiv.org/abs/1801.04381)
- Dataset: [PlantVillage Classification Dataset](https://www.kaggle.com/datasets/mohitsingh1804/plantvillage)

## Dataset
- **Total Images:** 54,000+ color images (224×224)
- **Classes:** 38 plant disease categories
- **Split:** ~43k training / ~10k testing samples

## Model Architecture
- **Structure:** 17 *Inverted Residual* blocks + 2 *Conv2D* layers + 1 *Fully Connected* layer (38 outputs)
- **Parameters:** 0.447M  
- **MACs:** 62.28M  

## Results
  | Metric | Train | Test |
  |---------|--------|------|
  | **Accuracy** | 99.56% | 99.34% |
  | **Latency** | — | 7 ms |
  | **Throughput** | — | 40,713 img/sec |
- **Training Time:** 50 minutes (with mixed precision)  
- **Visuals:** Accuracy / Loss curves and confusion matrix available in `results/`

## Key Takeaways
- Lightweight **MobileNetV2** variant achieves **state-of-the-art accuracy** on PlantVillage with **<0.5M parameters**.  
- **Mixed Precision** significantly reduces training time without accuracy loss.  
- Ideal for **resource-constrained devices** or **real-time plant disease detection**.
