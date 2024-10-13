# Student dropout prediction

![students](https://github.com/user-attachments/assets/63296c73-5b0a-43dc-961a-27b44be53216)

## Overview

This project aims to predict student dropout rates using Machine Learning Models with regularization, optimization, and Error analysis techniques used in machine learning to improve models' performance, convergence speed, and efficiency. The dataset used is processed and analyzed to train neural networks with different optimization techniques `(Adam and RMSProp)` to enhance model performance and generalization. In the project, I evaluated the rate of the students graduated and the students dropped out. I used publicly available dataset suitable for the project and then Implemented two types of Models, a vanilla model without any optimization techniques and another model with several optimization techniques.

## Model Development and Optimization Techniques

### Overview of Models and Techniques

The models used include a vanilla neural network, an L1 regularized model with Adam, and an L2 regularized model with RMSProp. The following optimization techniques were applied to improve performance:


## 1. Vanilla Model: Model with no optimizers

Test Loss: 1.6278

Test Accuracy: 0.6814

Accuracy: 0.6960 (highest among the models)

Precision: 0.6957

Recall (Sensitivity): 0.1622

Specificity: 0.9643

F1 Score: 0.2630

## 2. L1 Model with Adam Optimizer:

Test Loss: 0.6013 (significantly lower than Vanilla)

Test Accuracy: 0.7311 (higher than Vanilla)

Accuracy: 0.5548

Precision: 0.4149

Recall (Sensitivity): 0.8074 (much higher recall)

Specificity: 0.9643 (same as Vanilla)

F1 Score: 0.5482 (higher than Vanilla)

## 3. L2 Model with RMSProp Optimizer:

Test Loss: 0.5594 (lowest loss)

Test Accuracy: 0.7186 (higher than Vanilla)

Accuracy: 0.4734 (lower than Vanilla and L1)

Precision: 0.3803

Recall (Sensitivity): 0.9122 (highest recall)

Specificity: 0.9643 (same as Vanilla and L1)

F1 Score: 0.5368

## More Analysis:

Test Accuracy: L1 Model has the highest test accuracy at 0.7311, followed by L2 at 0.7186, both of which outperform the Vanilla model's 0.6814. Accuracy:

Vanilla Model has the highest accuracy at 0.6960, followed by L1 at 0.5548, and L2 trailing at 0.4734.

Precision: Vanilla has the best precision at 0.6957, meaning fewer false positives, while L1 and L2 perform lower in precision.

Recall (Sensitivity): Both L1 and L2 models drastically outperform the Vanilla model in terms of recall, with L2 achieving 0.9122 and L1 at 0.8074, compared to Vanilla's 0.1622.

F1 Score: L1 Regularization has the highest F1 Score of 0.5482, indicating a good balance between precision and recall.

L2 follows with an F1 Score of 0.5368, while Vanilla has the lowest F1 Score at 0.2630.

  ## Conclusion:

L1 Regularization with Adam is overall better than the Vanilla model. It has the highest test accuracy and F1 score, making it a more balanced model despite a slightly lower accuracy compared to Vanilla.

L2 Regularization, though it has excellent recall, does not surpass the L1 model or Vanilla in terms of accuracy or precision.

Thus, L1 Regularization offers the best performance overall compared to the Vanilla model, especially considering its superior test accuracy and F1 Score.


Here’s the performance comparison:

| Model            | Test Loss  | Accuracy  | Precision | Recall (Sensitivity) | F1 Score |
|------------------|------------|-----------|-----------|----------------------|----------|
| **Vanilla**       | 1.6278     | 69.60%    | 69.57%    | 16.22%               | 26.30%   |
| **L1 Regularized**| 0.6013     | 55.48%    | 41.49%    | 80.74%               | 54.82%   |
| **L2 Regularized**| 0.5594     | 47.34%    | 38.03%    | 91.22%               | 53.68%   |

The **L1 regularized model** outperformed the vanilla model in **test accuracy** by **5.06%** (73.11% vs. 68.14%) and also shows a significantly better balance between precision and recall, as indicated by the F1 score.
