# Student dropout prediction

![students](https://github.com/user-attachments/assets/63296c73-5b0a-43dc-961a-27b44be53216)

## Overview

The project aims to predict student dropout rates using machine learning models, with a focus on improving performance, convergence speed, and generalization through regularization, optimization, and error analysis techniques. The dataset used is publicly available and has been processed to train neural networks. The goal was to evaluate the rates of students who graduate versus those who drop out. For this, we developed two types of models: a baseline vanilla model (without any optimization) and models enhanced with regularization techniques and optimization algorithms like `Adam` and `RMSProp.`

### Model Development and Optimization Techniques

#### Overview of Models and Techniques
In this project, three different models were built to assess their effectiveness in predicting student dropout rates:

- **Vanilla Model**: This model does not use any optimization techniques. It serves as a baseline for comparing the effects of adding regularization and optimization to the models. 
- **L1 Regularized Model with Adam Optimizer**: In this model, L1 regularization is applied to reduce overfitting by penalizing the absolute value of the model's weights. The Adam optimizer is used for efficient learning and improved convergence.
- **L2 Regularized Model with RMSProp Optimizer**: This model uses L2 regularization, which stabilizes the training process by penalizing large weight values. The RMSProp optimizer is employed to help with faster convergence by adjusting learning rates based on recent gradient information.

### Optimization Techniques and Their Impact

#### Vanilla Model
The vanilla model, which does not use any optimizers, acts as a benchmark for the project. The absence of regularization or an advanced optimizer limits its ability to generalize well to new data. As a result, while the vanilla model achieves a moderate test accuracy, it suffers from a low recall, indicating that it struggles to identify students at risk of dropping out. The high test loss further suggests that the model may be overfitting the training data.

#### L1 Regularized Model with Adam Optimizer
This model improves significantly over the vanilla baseline due to two key elements: **L1 regularization** and the **Adam optimizer**.

- **L1 regularization** introduces a penalty based on the absolute values of the model’s weights. This helps drive some of the weights to zero, effectively simplifying the model and preventing overfitting. By penalizing large coefficients, L1 regularization forces the model to focus on the most important features, leading to better generalization.
  
- **Adam optimizer** is a combination of two popular optimization algorithms, AdaGrad and RMSProp. It computes individual learning rates for each parameter based on estimates of first and second moments of the gradients. Adam adjusts learning rates dynamically during training, resulting in faster convergence and a more efficient update process.

With the combination of L1 regularization and Adam, this model shows a marked improvement in both test accuracy and recall. The recall value is significantly higher than the vanilla model, meaning it is much better at identifying students who are likely to drop out. The F1 score, which balances precision and recall, is also much higher, showing that this model strikes a good balance between correctly identifying at-risk students while minimizing false positives.

#### L2 Regularized Model with RMSProp Optimizer
This model applies **L2 regularization** and uses the **RMSProp optimizer** to enhance performance.

- **L2 regularization** adds a penalty proportional to the square of the weights. Unlike L1, which drives some weights to zero, L2 regularization tends to shrink the weights more smoothly. This results in a more stable training process, as the model is discouraged from assigning overly large weights to any particular feature, which could cause overfitting.

- **RMSProp optimizer** adjusts the learning rate of each parameter individually by maintaining a running average of recent gradient magnitudes. This technique is particularly effective when dealing with noisy or complex data because it helps prevent oscillations and ensures smoother convergence.

While the L2 regularized model performs well in terms of recall (the highest among all models), indicating a strong ability to correctly identify students at risk of dropping out, it falls slightly behind the L1 model in terms of accuracy and precision. This suggests that although the model is very good at identifying at-risk students, it may also include more false positives than desired.

### Analysis of Model Performance
- **Test Accuracy**: The L1 regularized model outperforms both the vanilla and L2 models in terms of accuracy. This means that overall, the L1 model is better at making correct predictions across the entire dataset.
  
- **Recall**: Both L1 and L2 models drastically outperform the vanilla model when it comes to recall, with the L2 model excelling in this metric. Higher recall means these models are more capable of identifying students who are actually at risk of dropping out.

- **F1 Score**: The L1 model achieves the highest F1 score, which indicates the best balance between precision (avoiding false positives) and recall (correctly identifying true positives). This makes the L1 model the most well-rounded in terms of performance.

### Conclusion
- **L1 Regularized Model with Adam** is the best-performing model overall. It improves upon the vanilla model significantly, especially in recall and F1 score. The use of L1 regularization simplifies the model by focusing on important features, while Adam accelerates training and convergence. This combination results in a model that is both accurate and well-generalized.
  
- **L2 Regularized Model with RMSProp** also shows strong performance, particularly in recall, making it effective at identifying students at risk of dropping out. However, it does not surpass the L1 model in terms of accuracy or precision.

In summary, regularization techniques (L1 and L2) combined with advanced optimizers (Adam and RMSProp) significantly enhance model performance compared to a vanilla model with no optimization. In particular, L1 regularization with Adam offers the best balance between accuracy, precision, and recall, making it the most suitable model for predicting student dropout rates.


### How to Run

To set up and run the project, follow these steps:

1. **Clone the repository**  
   Clone the repository to your local machine using the following commands:

   ```bash
   https://github.com/MohamedAYasin/student-dropout-prediction_summative.git
   
   ```

2. **Create a Virtual Environment**

It’s recommended to create a virtual environment to manage dependencies. You can use either `venv` or `conda`:

- **Using `venv`:**

```bash
  python3 -m venv venv
  source venv/bin/activate   # On macOS/Linux
  venv\Scripts\activate      # On Windows
```

- **Using conda:**

```bash
conda create --name your_env_name python=3.8
conda activate your_env_name
```

3. **Install Dependencies**

Install the required dependencies listed in `requirements.txt`:

```bash
pip install -r requirements.txt
```
