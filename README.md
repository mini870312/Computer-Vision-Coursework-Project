# PCA Analysis with KNN Classifiers


The figure below presents the MNIST classification results using KNN with Euclidean and Mahalanobis distances across varying numbers of PCA components, with each line representing a different choice of k values. When the number of components is reduced to 2, the classification accuracy for both distance metric falls below 50%. However, accuracy increases sharply, surpassing 90% at 30 and 50 components. Specifically, the highest accuracy of 97.76% is achieved with 50 PCA components using Euclidean distance, while Mahalanobis distance reaches its peak accuracy of 97.12% with 30 components; both peak accuracies occur when k=3. Beyond this point, the accuracy with Euclidean distance remains stable as the number of components increases, whereas the accuracy with Mahalanobis distance gradually declines, dropping below 60% at 500 components and maintaining low accuracy thereafter across all k values.

 
<img width="755" alt="image" src="https://github.com/user-attachments/assets/203ae4ec-cf91-4aab-8669-2cc723f0e155" />


On the other hand, the Fashion MNIST dataset exhibits a similar trend in classification accuracy under the same conditions, with different KNN classifiers and both distance metrics reaching their peak performance before 100 PCA components. The highest accuracy achieved is 86.06% with Euclidean distance and 85.69% with Mahalanobis distance, both at k=5, which are notably lower than the peak accuracies observed on MNIST. As the number of PCA components increases, the accuracy with Euclidean distance remains stable above 85%, whereas the accuracy with Mahalanobis distance declines significantly, dropping below 60% at the highest number of components evaluated across all k values.

<img width="770" alt="image" src="https://github.com/user-attachments/assets/836ce87b-2087-4a1b-bee9-62ec971c22e9" />

These results indicate that for both datasets, using 50 or 100 PCA components yields optimal classification accuracy under both the given settings. This can be attributed to PCA’s ability to analyze and retain the most significant component—those with the largest eigenvalues—while discarding less informative dimensions. As a result, the classifier becomes more effective at capturing the essential characteristics of the data.

Dimensionality reduction techniques such as PCA are crucial for improving computational efficiency, especially in high-dimensional classification problems. PCA not only facilitates data compression, but also enables the classifier to process data more efficiently without compromising performance. Therefore, integrating PCA into classification workflows can enhance both accuracy and computational speed, making it an effective preprocessing step for high-dimensional data classification tasks.
