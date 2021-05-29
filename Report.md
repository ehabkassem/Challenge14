We were assumed to be a financial advisor and we had to use machine learning models to make optimum trading decisions. A number of short tasks were provided to us and we had to complete the left out places for code. The challenge also involved making suitable decisions at different along with it's documentation that would explain why a particular decision was made. 
Following are the some of the points required for this evaluation report:
# TRAINING SIZE HYPER TUNING
Effect of changing the training size on accuracy score:
training month = 2: acc = 54.38
training month = 3: acc = 54.43
training month = 4: acc = 52.40
training month = 5: acc = 53.34

Training month = 3 gave the best accuracy as the other durations were either too long or too short.

A piece of code was written to find the best hyper parameters for the model. The best accuracy score achieved for svm was 0.559
The set of parameters that gave the best accuracy turned out to be: 
kernel = linear, gamma = auto, probability = True

# SMA WINDOW TUNING:
short window = 6, long window = 100, accuracy =  56.1
short window = 7, long window = 100, accuracy =  54.8
short window = 8, long window = 100, accuracy =  56.45
short window = 9, long window = 100, accuracy =  56.28
short window = 9, long window = 102, accuracy =  56.4
short window = 9, long window = 105, accuracy =  55.8
short window = 9, long window = 104, accuracy =  56.1
short window = 9, long window = 90, accuracy = 56.45
short window = 5, long window = 90, accuracy = 56.25
short window = 5, long window = 105, accuracy =  56.46
short window = 7, long window = 105, accuracy =  56.1
short window = 8, long window = 105, accuracy =  56.07

short window = 5, long window = 105 gave the best accuracy of 56.46

It was then observed that the the short window size should be small to capture recent trends and long window size should be large to get better historical data.

# ADABOOST CLASSIFIER:
Adaboost classifier was added with the intention to analyze it's performance against the given data. It was found that the AdaBoost classifier didn't give better results when compared to SVM. This makes sense as SVMs are large margin classifiers. Adaboost gave an accuracy of 55.1 which is close to 55.46 of SVM. If the features columns have been more, AdaBoost would have outperformed SVM.

# PARAMETER HYPER TUNING:
Grid Search approach was used for hyper tuning as the parameters and their possibilites were less in number. A piece of code was written that training and tested the model for the brute forced hyper parameters. The results were recorded and best parameters were then picked out. Since there were only a few columns in the dataset, the changes were not that big. After using hyper tuning the accuracy of test set increased for almost 4% for both the models.