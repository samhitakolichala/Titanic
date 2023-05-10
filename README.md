# car-evaluation

**Car Evaluation Dataset**

**Dataset Description**

The Car Evaluation Dataset contains information about different cars and their attributes. There are six attributes:

Buying: Buying price of the car (vhigh, high, med, low)
Maint: Maintenance price of the car (vhigh, high, med, low)
Doors: Number of doors (2, 3, 4, 5more)
Persons: Capacity in terms of persons to carry (2, 4, more)
Lug_boot: The size of luggage boot (small, med, big)
Safety: Estimated safety of the car (low, med, high)
There are four classes for each car, which indicate its acceptability:

unacc: Unacceptable
acc: Acceptable
good: Good
vgood: Very Good
The dataset contains 1728 instances.

**Insights Gained**

 Here are some possible insights we can gain:

Most cars are in the "unacc" class, followed by "acc", "good", and "vgood".
Cars with high buying and maintenance prices are more likely to be in the "vgood" class.
Cars with more doors and a larger luggage boot are more likely to be in the "vgood" class.
Cars with high safety ratings are more likely to be in the "good" and "vgood" classes.

**Method**

We can use a classification algorithm to predict the acceptability of a car based on its attributes. We can split the dataset into training and testing sets into 80:20 ratio , and use the training set to train the algorithm and the testing set to evaluate its performance.

We can use the Decision tree classifier,extra tree classifier,Random Forest classifier. Amongst which 'Extra tree classifier' performed well.

**Evaluation**

We can evaluate the performance of the algorithm using accuracy, precision, recall, and F1 score. Since the dataset is imbalanced, I used 'undersampling'.

**Results**

After training and testing the Extra tree classifier algorithm on the Car Evaluation Dataset, we obtained the following results:

training      precision    recall  f1-score   support

           0       0.94      0.74      0.83        39
           1       0.78      0.62      0.69        34
           2       1.00      0.97      0.99        38
           3       0.71      1.00      0.83        39

    accuracy                           0.84       150
   macro avg       0.86      0.83      0.83       150
weighted avg       0.86      0.84      0.84       150



testing           precision    recall  f1-score   support

           0       0.80      1.00      0.89         8
           1       1.00      0.46      0.63        13
           2       1.00      1.00      1.00         9
           3       0.62      1.00      0.76         8

    accuracy                           0.82        38
   macro avg       0.85      0.87      0.82        38
weighted avg       0.88      0.82      0.80        38

These results indicate that the algorithm performs well on the dataset and can accurately predict the acceptability of a car based on its attributes.
