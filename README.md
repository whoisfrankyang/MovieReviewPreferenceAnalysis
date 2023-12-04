# MovieReviewPreferenceAnalysis
ML Sentiment Analysis Project

Data Preprocessing:
After we import the data, we performed the train, validation split of 8:2. We implemented the data augmentation via noise injection increase the data sample from 15000 to 45000 samples. The noise is sampled from a normal distribution. Then, we perform feature engineering, introducing 4 new features: differential feature, cosine similarities, mean, and variance. 

Model Selection
We tried 3 different classifiers: logistic regression, SVM, and ANN. For LR, we set the C=10. For SVM, we set C=2. For the neural net architecture, it has a dense layer with 16 neurons, relu activation function, and an output layer with sigmoid activation function. We also applied batch normalization and dropout layer to reduce the overfitting. The optimizer is Adam with learning rate = 0.001. We also tried the SGD, but its performance is worse than Adam. The batch size is 300. After fine tuning these 3 classifiers, we showed that SVM has the best performance. 

In addition, we also tried to apply PCA to reduce the feature dimensionality, but it was unsuccessful. 
