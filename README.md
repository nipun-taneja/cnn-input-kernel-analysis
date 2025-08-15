# CNN Input Size and Kernel Size Experiments on MNIST

Investigate how input resolution and convolutional kernel size affect the performance of convolutional neural networks (CNNs) on the MNIST dataset.

---
## Objective
- Quantify the effect of shrinking input image size on model accuracy.
- Analyze how kernel size impacts feature extraction and generalization.
- Provide practical guidelines for CNN design.

---
## Methodology

### Experiment 1 — Input Sizes
- Resized MNIST images to: 28×28, 24×24, 20×20, 14×14, 10×10, 8×8, 6×6, 3×3.
- Trained CNN models for 10 epochs at each resolution.
- Compared validation accuracy across configurations.

### Experiment 2 — Kernel Sizes
- Trained CNNs with kernel sizes: 1×1, 3×3, 5×5, 7×7, 9×9, 12×12.
- Trained for 10 epochs per configuration.
- Compared validation accuracy across kernel sizes.

---

## Results

### Experiment 1 — Input Sizes
- Larger inputs (28×28) yield the best accuracy.
- Accuracy decreases as size shrinks, especially below 10×10.
- Extremely small inputs (3×3, 6×6) strip away meaningful features
<img width= 75% height="547" alt="image" src="https://github.com/user-attachments/assets/dac1f997-1f05-43a4-89a3-549e514271fc" />

### Experiment 2 — Kernel Sizes
- 3×3 and 5×5 kernels perform best, balancing receptive field and efficiency.
- Very small (1×1) kernels underperform due to limited context.
- Very large (≥9×9) kernels degrade performance by oversmoothing and adding unnecessary parameters.
<img width= 75% height="314" alt="image" src="https://github.com/user-attachments/assets/6169623f-8ab1-4964-920f-6b00bac3a2be" />

---

## Key Findings
- Input size trade-off: smaller inputs speed up training but reduce accuracy. Do not shrink below 14×14 for MNIST-level complexity.
- Kernel size sweet spot: 3×3 and 5×5 kernels are optimal choices for CNNs.
- Practical guideline: preserve enough input resolution and avoid oversized kernels to balance accuracy and efficiency.

---

## How to Run
Run in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nipun-taneja/cnn-input-kernel-analysis/blob/main/Experiment_01.ipynb)

---

## Author
Nipun Taneja – MS in Artificial Intelligence, San Francisco State University  
[LinkedIn](https://www.linkedin.com/in/nipun-taneja) | [GitHub](https://github.com/nipun-taneja)
