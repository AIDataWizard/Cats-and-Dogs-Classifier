# Cats-and-Dogs-Classifier

This project involves using the Cats and Dogs dataset containing 99 images each of cats and dogs, all at a resolution of 64x64 pixels. The dataset is structured as a 198x4096 matrix, with label 0 for cats and label 1 for dogs. Our task involves conducting simulation studies to compare a variety of classification methods—including kNN, DA methods, logistic regression, lasso regression, kernel-based methods like KRR and SVMs, ensemble methods like RF and GBM, and neural networks—under different sample sizes. 

The goal is to explore the advantages and disadvantages of these methods in various settings, particularly focusing on how their performance is influenced by the size of the sample. We are required to run simulations multiple times across at least three different sample sizes, analyze the classification accuracy, identify consistent misclassifications, and determine the importance of specific pixels in the classification process. 

The findings will provide insights into the robustness and reliability of each method under varying conditions of data complexity and sample size.

# Section 1. Studying the Data
We initiate our analysis by meticulously reviewing the data and photographs, followed by a precise 90° clockwise rotation of the images. This phase also involves the correction of any mislabeling and the systematic scaling of the data to ensure accuracy and consistency.

![Cats and Dogs Dataset Images](https://github.com/AIDataWizard/Cats-and-Dogs-Classifier/blob/main/Images/Cats%20and%20Dogs%20Pictures.PNG)

# Section 2. Model Training and Hyperparameter Tuning 
Five classifiers—kNN, Logistic Regression, SVM, Random Forest, and xgBoost—were employed to analyze the Cats and Dogs dataset. GridsearchCV extracts the best perameters for the models on the dataset. The following graph shows classification accuracy before and after hyperparameter tuning.

![Classification Accuracy Before and After Hyperparameter Tuning](https://github.com/AIDataWizard/Cats-and-Dogs-Classifier/blob/main/Images/Classification%20Accuracies.png)

## Also utilized confusion matrices and classification reports for much deeper comparison:
  1. Precision: SVM shows the highest precision, suggesting a lower false positive rate overall.
  2. Recall: SVM also shows the highest recall, indicating a lower false negative rate overall.
  3. F1-Score: SVM has the highest F1-Score, suggesting a better balance between precision and recall.

## Most commonly misclassified images on all the models are illustrated below:

![Most commonly misclassified images](https://github.com/AIDataWizard/Cats-and-Dogs-Classifier/blob/main/Images/Misclassified%20Images.png)

## Why are these images difficult to classify ?
- Ambiguous Features: The misclassified images actually show dogs that have features that could be mistaken for either cats or a different breed of dog. For example, the dogs have varying fur patterns and the facial structures like the "pointy" ears and gap between ears that confuse the classifier
- Low Resolution: 64 x 64 pixels are low resolution images, which means that finer details that could help in classifying between dogs and cats are lost.

# Section 3. Determining the most important pixels for classification using ANOVA
There are multiple methods to recognize the most important features such as Filter Based Feature Selection (ANOVA F-test). The figure below actually shows the important features that contribute the most in classification of cats and dogs. 

![ANOVA F-test Important Features](https://github.com/AIDataWizard/Cats-and-Dogs-Classifier/blob/main/Images/ANOVA%20F-test.png)

## Are these features easy to identify or is there uncertainty in the selection of important features ?
- There is considerable uncertainty in feature selection as different methods identify different sets of important features.
- Ovearlapping: Some features are identified as important across multiple methods, which can increase confidence in their importance.
- The importance scores and visualizations indicate relative importance but do not provide absolute certainty.

# Section 4. Clustering the Whole Dataset (Assuming there are no labels provided)
We use 3 clustering algorithms here: Gaussian Mixture, K-Means and Agglomerative

![GMM with 6 clusters](https://github.com/AIDataWizard/Cats-and-Dogs-Classifier/blob/main/Images/GMM%206%20Cluster.png)

Looking at the datapoints from different PCA dimensions, the following figure shows clustered data:

![Clustered Dataset](https://github.com/AIDataWizard/Cats-and-Dogs-Classifier/blob/main/Images/Clustered%20Data%20points.png)

The comprehensive analysis of these classifiers highlighted their relative strengths and weaknesses, offering a clear understanding of how each method performs under varying conditions and providing a basis for selecting the most suitable classifier for similar classification tasks.
