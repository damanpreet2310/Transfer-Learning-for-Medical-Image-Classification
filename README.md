# Transfer Learning for Medical Image Classification

In this project, we leverage **transfer learning techniques**, which involve using models trained on large datasets, to improve the performance of diabetic retinopathy detection. The goal is to enhance detection accuracy by fine-tuning models and understanding classification results through visualizations and explainable AI.

---

## Project Overview

The project consists of **5 main tasks**. The idea is to generate `test_predictions.csv` files for each task and check the scores on Kaggle.

### Tasks Overview

#### a) Fine-Tune a Pretrained Model
- Fine-tune a pretrained **ResNet18** model (trained on ImageNet) using the **DeepDRiD dataset**.
- Experiment with different **data augmentation techniques** to improve the model's robustness.
- **Note:** The reference architecture used in this report is based on single-image input.

#### b) Two-Stage Training with Additional Datasets
1. **Stage 1:**
   - Fine-tune the pretrained **ResNet18** model using a larger dataset (**Kaggle DR Resized**).
   - Save the resulting **stage1 model**.
2. **Stage 2:**
   - Fine-tune the **stage1 model** on the **DeepDRiD dataset**.
   - Evaluate the **stage2 model** and generate `test_predictions.csv`.
   - Check the Kaggle score for the predictions.

#### c) Incorporate Attention Mechanisms
- Enhance the **ResNet18** model with **multi-head attention mechanisms** while fine-tuning on the **DeepDRiD dataset**.
- Experiment with:
  - **With/without layer normalization**
  - **With/without residual connections**

#### d) Ensemble Learning
- Use the **bagging technique**:
  - Load pretrained weights provided for models like `efficientnet_b0`, `resnet18`, and `resnet34`.
  - Fine-tune each model on the **DeepDRiD dataset**.
- Combine predictions from the models (`test_predictions.csv` for each) using bagging to generate the final `test_predictions.csv`.
- Upload the final predictions to Kaggle.

---

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/damanpreet2310/Transfer-Learning-for-Medical-Image-Classification.git)
   cd Transfer-Learning-for-Medical-Image-Classification
