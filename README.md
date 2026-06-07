# Rice Leaf Disease Classification Framework

This repository contains a Deep Learning and Explainable AI (XAI) framework designed to identify and classify four major rice leaf diseases: **Bacterial Blight, Blast, Brown Spot, and Tungro**. 

Our framework evaluates and compares three different convolutional neural network architectures to balance high classification accuracy with computational efficiency for real-world agricultural deployment.

## 📂 Project Structure

* `notebook121e7db419.ipynb` - The primary Jupyter Notebook containing the full pipeline (Data preprocessing, Model training, and XAI evaluations).
* `Figures/` - A dedicated folder containing all our finalized visual outputs, curves, confusion matrices, and XAI heatmaps.
* `Tables/` - A dedicated folder containing our final model evaluation tables and performance metrics.

## 🤖 Deep Learning Models Evaluated

1.  **Custom CNN:** A standalone model built entirely from scratch to establish a baseline for leaf disease detection.
2.  **MobileNetV2:** A lightweight, highly efficient transfer learning model optimized for speed and edge-device/mobile performance.
3.  **ResNet50:** A deep residual architecture leveraging skip connections for high-capacity pattern recognition.

## 📈 Key Results & Metrics

Our benchmarks showed that **MobileNetV2** is the optimal model for this deployment scenario, combining flawless accuracy with lightweight resource requirements.

| Model Architecture | Accuracy | Total Parameters | Training Time |
| :--- | :---: | :---: | :---: |
| **MobileNetV2** | **99.92%** | **2.26M** | **94.62s** |
| **Custom CNN** | 96.12% | 22.2M | 854.00s |
| **ResNet50** | 94.13% | 23.5M | *Frozen Baseline* |


To ensure our AI makes decisions based on genuine pathological features rather than background noise, we integrated two distinct visual explanation techniques:

* **Grad-CAM:** Generates intuitive, region-level visual heatmaps displaying the exact focus areas of the model. Perfect for quick validation by field workers or farmers.
* **SHAP:** Provides granular, pixel-level definitions mapping out precise object boundaries. This allows researchers to verify that the network is tracking leaf lesions accurately.

*All final visualization charts are located inside the `Figures/` directory, and data metrics are inside the `Tables/` directory.*
