Logistic regression is a classification algorithm used to predict the probability that an instance belongs to a particular class. Despite its name, logistic regression is primarily used for binary classification tasks, where the target variable has two possible outcomes. However, it can be extended to handle multi-class classification problems as well using techniques like one-vs-rest or multinomial logistic regression.

### Logistic Function (Sigmoid Function):

The logistic regression model makes predictions using the logistic function (also known as the sigmoid function), which maps any real-valued number to the range [0, 1]. The logistic function is defined as:

\[ \sigma(z) = \frac{1}{1 + e^{-z}} \]

![image](https://github.com/vansh-py04/Machine-Learning-Algorithms-from-Scratch/assets/128248352/860092a1-2632-491b-8c0b-2fc3e6810f19)

Where:
- \( \sigma(z) \) is the logistic function.
- \( z \) is the linear combination of input features and their corresponding coefficients, often denoted as \( \mathbf{w}^T\mathbf{x} + b \), where \( \mathbf{w} \) represents the weight vector, \( \mathbf{x} \) represents the input features, and \( b \) is the bias term.

The logistic function transforms the output of the linear combination into a probability score, which can be interpreted as the likelihood of belonging to the positive class (class 1).

### Probability Prediction:

Given the logistic function, the probability that an instance \( \mathbf{x} \) belongs to the positive class (class 1) is calculated as:

\[ P(y = 1 | \mathbf{x}; \mathbf{w}, b) = \sigma(\mathbf{w}^T\mathbf{x} + b) \]

Similarly, the probability of belonging to the negative class (class 0) is:

\[ P(y = 0 | \mathbf{x}; \mathbf{w}, b) = 1 - P(y = 1 | \mathbf{x}; \mathbf{w}, b) \]

### Cost Function (Cross-Entropy Loss):

To train a logistic regression model, we need a suitable cost function to measure the difference between the predicted probabilities and the actual labels. The commonly used cost function for logistic regression is the cross-entropy loss (also known as log loss or binary cross-entropy loss), defined as:

\[ J(\mathbf{w}, b) = -\frac{1}{m} \sum_{i=1}^{m} [y^{(i)} \log(\hat{y}^{(i)}) + (1 - y^{(i)}) \log(1 - \hat{y}^{(i)})] \]

![image](https://github.com/vansh-py04/Machine-Learning-Algorithms-from-Scratch/assets/128248352/de5eb90b-4c69-48d9-83b8-e5f8c26640e4)

Where:
- \( m \) is the number of training examples.
- \( y^{(i)} \) is the actual label (0 or 1) for the \( i \)-th training example.
- \( \hat{y}^{(i)} \) is the predicted probability that the \( i \)-th example belongs to the positive class.
- \( J(\mathbf{w}, b) \) is the cross-entropy loss.

The goal of training is to minimize the cross-entropy loss by adjusting the model parameters (weights \( \mathbf{w} \) and bias \( b \)).

### Gradient Descent:

To minimize the cost function, gradient descent is typically used. The gradients of the cost function with respect to the model parameters are computed, and the parameters are updated iteratively in the opposite direction of the gradient until convergence.

![image](https://github.com/vansh-py04/Machine-Learning-Algorithms-from-Scratch/assets/128248352/ec2e85fc-8a7c-4872-b4b2-51a0a6d72588)

### Visualization:

![image](https://github.com/vansh-py04/Machine-Learning-Algorithms-from-Scratch/assets/128248352/f73700c7-ad71-44e3-803b-5b1119719224)
