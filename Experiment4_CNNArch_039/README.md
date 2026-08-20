# Experiment 4 — CNN Transfer Learning

This experiment studies major CNN architectures including **LeNet-5, AlexNet, VGG16, GoogleNet, and ResNet**, followed by **Transfer Learning using ImageNet-pretrained ResNet50** on the CIFAR-10 dataset.

### Dataset

* **CIFAR-10**
* 50,000 training images
* 10,000 test images
* Image size: 32 × 32 × 3
* 10 classes

### Main Work

* CNN architecture comparison
* Transfer learning with ResNet50
* Frozen-base training
* Fine-tuning
* Model evaluation
* Confusion matrix and performance analysis

### Result

The fine-tuned ResNet50 achieved:

* **Validation Accuracy:** 91.38%
* **Test Accuracy:** 90.55%
* **Weighted F1-score:** 0.9053

### Files

* `Experiment_4_CNN_Transfer_Learning.ipynb` — Implementation and experiments
* `Experiment_4_Report.tex` — LaTeX report
* `Experiment_4_Report.pdf` — Final report
* `figures/` — Generated plots and visualizations
