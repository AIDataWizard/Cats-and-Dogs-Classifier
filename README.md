# Cats-and-Dogs-Classifier

This project involves using the Cats and Dogs dataset containing 99 images each of cats and dogs, all at a resolution of 64x64 pixels. The dataset is structured as a 198x4096 matrix, with label 0 for cats and label 1 for dogs. Our task involves conducting simulation studies to compare a variety of classification methods—including kNN, DA methods, logistic regression, lasso regression, kernel-based methods like KRR and SVMs, ensemble methods like RF and GBM, and neural networks—under different sample sizes. 

The goal is to explore the advantages and disadvantages of these methods in various settings, particularly focusing on how their performance is influenced by the size of the sample. We are required to run simulations multiple times across at least three different sample sizes, analyze the classification accuracy, identify consistent misclassifications, and determine the importance of specific pixels in the classification process. 

The findings will provide insights into the robustness and reliability of each method under varying conditions of data complexity and sample size.

Five classifiers—kNN, Logistic Regression, SVM, Random Forest, and xgBoost—were employed to analyze the Cats and Dogs dataset. The project involved several key steps:

  1. Classification Performance: The classification accuracy of each method was evaluated on the dataset. Resampling techniques were used to assess the robustness of each classifier and identify images that were consistently misclassified.

  2. Feature Importance: The most important pixels for classification were identified, and methods for feature selection were compared to understand the stability of these selections across different classifiers.

  3. Clustering Analysis: The dataset was clustered to determine if the resulting clusters aligned with the class labels, and the impact of varying the number of clusters on this alignment was examined.

  4. Simulation Studies: Simulation studies were conducted by creating different sample sizes and repeating the classification tasks multiple times to observe how each classifier's performance varied with sample size. These simulations provided insights into the advantages and disadvantages of each classifier depending on the complexity of class separation and the amount of available data.

The comprehensive analysis of these classifiers highlighted their relative strengths and weaknesses, offering a clear understanding of how each method performs under varying conditions and providing a basis for selecting the most suitable classifier for similar classification tasks.
