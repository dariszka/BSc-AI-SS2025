# A1 - Estimation Theory, Fisher Information, CRLB

### Overview
This assignment focuses on **Estimation Theory**, covering topics such as **log-likelihood functions**, **Fisher Information**, **Cramér-Rao Lower Bound (CRLB)**, and **efficiency** of estimators. The tasks involved theoretical derivations and implementing these concepts to evaluate the properties of estimators in statistical models.

### Key Tasks

- **Log-Likelihood and Estimators**  
  - Implemented the log-likelihood function for Gaussian data and tested it with different values of \(\sigma\).
  - Derived the **unbiasedness** of the sample mean as an estimator for the population mean \(\mu\).

- **Fisher Information and CRLB**  
  - Computed **Fisher Information** for \(\mu\) and confirmed that the **Cramér-Rao Lower Bound** is reached, proving the efficiency of the sample mean estimator.
  - Verified the variance of the estimator and compared it to the CRLB, showing that the sample mean is an **efficient estimator**.

- **Unbiasedness and Efficiency**  
  - Showed that the arithmetic mean estimator for \(\mu\) is unbiased.
  - Checked the efficiency of the estimator by proving that its variance equals the CRLB.
  
---

# A2 - Maximum Likelihood

### **Overview**
This assignment explores **Maximum Likelihood Estimation (MLE)** for a Poisson-distributed dataset, focusing on analytical derivation, numerical optimization, and visualization of the log-likelihood function.

### **Key Tasks**

- **Analytical Estimation and Optimization**  
  - Derived the MLE for the Poisson rate parameter \( \lambda \) using calculus.  
  - Implemented a function to compute the MLE analytically.
  - Estimated \( \lambda \) numerically by maximizing the log-likelihood over a discrete set of values.  

- **Log-Likelihood Visualization**  
  - Plotted the log-likelihood function over a range of \( \lambda \) values.  
  - Marked and compared the analytical and numerical MLE estimates.

---
# A3 - PCA

### **Overview**  
This assignment focuses on **implementing Principal Component Analysis (PCA) from scratch**, applying it to the Iris dataset to explore dimensionality reduction and variance preservation.

### **Key Tasks**  

- **Data Preprocessing and Exploration**  
  - Loaded and visualized the Iris dataset using histograms to analyze feature distributions across classes.  

- **Covariance Matrix and Eigen Decomposition**  
  - Computed the covariance matrix to quantify relationships between features.  
  - Performed eigen decomposition to obtain eigenvalues and eigenvectors.

- **Dimensionality Reduction with PCA**  
  - Sorted eigenpairs by explained variance and selected the top principal components.  
  - Projected the dataset onto a **lower-dimensional subspace (2D)** while retaining maximum variance.
  

