# deep-learning-challenge

### Overview of the Analysis

This analysis aims to build a deep learning model using TensorFlow and Keras to forecast which applicants are most likely to succeed if funded by Alphabet Soup, a nonprofit organization. The objective is to develop a predictive tool based on historical data from previous funding applications, enabling the organization to identify applicants with high potential for success and thereby enhance resource allocation efficiency.

### Results

#### Data Preprocessing

- **Target Variable(s):**
  - **IS_SUCCESSFUL:** Indicates the success (1) or failure (0) of the funding application.
  
- **Feature Variables:**
  - All columns except for EIN and NAME were used as features.

- **Variables Removed:**
  - **EIN** and **NAME** were excluded as they were irrelevant to the model.

#### Compiling, Training, and Evaluating the Model

- **Neurons, Layers, and Activation Functions:**
  - **Input Layer:**
    - **Neurons:** 100
    - **Activation Function:** Swish
  - **Hidden Layers (5 additional layers):**
    - **Neurons:** 80, 60, 60, 60, 60
    - **Activation Function:** ReLU
  - **Output Layer:**
    - **Neurons:** 1
    - **Activation Function:** Sigmoid

- **Target Model Performance:**
  - The goal was to achieve an accuracy of 75% or higher. However, after some tinkering, the best accuracy achieved was around 73%.

- **Steps to Increase Model Performance:**
  - Removed unnecessary features.
  - Binned data from other features and created cutoff values.
  - Experimented with various activation functions (ReLU, LeakyReLU, SELU, ELU, Swish, Tanh) in different combinations.
  - Increased the number of units in the input layer from 80 to 100.
  - Tested different numbers of units (80, 60) in the hidden layers.
  - Added more layers in some versions.
  - Applied L2 regularization with a coefficient of 0.001.
  - Used various optimizers (Adam, SGD, RMSprop, Nadam) with Adam being the most effective, followed by SGD.
  - Implemented early stopping, learning rate scheduling, and model checkpointing to optimize training.
  - Tested numerous combinations of neurons, activation functions, layers, and optimizers, including versions without feature removal and different binning strategies.

### Summary

This deep learning model achieved a maximum accuracy of approximately 73% in predicting the success of applicants funded by Alphabet Soup. Despite extensive optimization efforts, including modifying activation functions, network architecture, and optimizers, the performance improvement was minimal, with accuracy consistently ranging between 72% and 73%.

With additional time and further exploration of the dataset, better results could potentially be achieved by experimenting with diverse combinations of the aforementioned methods. Although these were the highest results obtained in this analysis, future advancements in deep learning predictability may lead to improved outcomes.
