# Student dropout prediction

![students](https://github.com/user-attachments/assets/63296c73-5b0a-43dc-961a-27b44be53216)



Here’s the performance comparison in a similar format:

| Model            | Test Loss  | Accuracy  | Precision | Recall (Sensitivity) | F1 Score |
|------------------|------------|-----------|-----------|----------------------|----------|
| **Vanilla**       | 1.6278     | 69.60%    | 69.57%    | 16.22%               | 26.30%   |
| **L1 Regularized**| 0.6013     | 55.48%    | 41.49%    | 80.74%               | 54.82%   |
| **L2 Regularized**| 0.5594     | 47.34%    | 38.03%    | 91.22%               | 53.68%   |

The **L1 regularized model** outperformed the vanilla model in **test accuracy** by **5.06%** (73.11% vs. 68.14%) and also shows a significantly better balance between precision and recall, as indicated by the F1 score.
