1- The part 2 of data preparation:

 After loading the CSV dataset "PRECISION90.csv" we performed =>

   a* Missing Values Imputation
   b* Feature Scaling 
   c* Encoding Categorical Data 

2- Modeling :

After meticulously preprocessing our dataset, we moved to the modeling phase, aiming to
develop machine learning models capable of accurately identifying gender based on the extracted
voice characteristics. This stage involved the selection, training, and evaluation of various models (supervised and unsupervised).

   A. Supervised Algorithms :

      1. Support Vector Machines (SVM): Explored with four different kernels:
        •Linear Kernel.
        •Polynomial Kernel.
        •Radial Basis Function (RBF) Kernel.
        •Sigmoid Kernel.

      2. k-Nearest Neighbors (k-NN).
      3. Random Forest.
      4. XGBoost.

   B. Unsupervised Algorithms :
      1. K-Means Clustering.
      2. Gaussian Mixture Models (GMM).

To assess model performance, we used the accuracy, precision, recall, and F1-score metrics,
derived from the confusion matrix,

In addition to the standard evaluation metrics, we also included inference time, which is the
duration required for a trained model to make a prediction once it’s deployed for real-worlduse.
