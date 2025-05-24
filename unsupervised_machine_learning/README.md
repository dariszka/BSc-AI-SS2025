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

---

# A4 - PCA and Kernel PCA

### **Overview**  
This assignment explores **Principal Component Analysis (PCA)** and **Kernel PCA**, with a focus on variance maximization, dimensionality reduction, and handling nonlinear structures. 

### **Key Tasks**  

- **Theoretical Properties of PCA**  
  - Proved that the covariance matrix is positive semi-definite and explained why this guarantees non-negative eigenvalues.
  - Interpreted the role of eigenvalues in PCA as measures of variance captured by each principal component.

- **PCA for Image Compression**  
  - Applied PCA to compress facial image data from 2250 dimensions to preserve **50%**, **75%**, and **99%** of total variance.
  - Reconstructed and visualized images at different compression levels to evaluate visual quality and variance retention.

- **2D PCA Visualization**  
  - Performed PCA on two low-dimensional datasets and visualized the principal components over the original data.
  - Computed and displayed the **explained variance ratio** to analyze how much information is retained by each component.

- **Kernel PCA with Polynomial and RBF Kernels**  
  - Implemented Kernel PCA using both **polynomial** and **RBF (Gaussian)** kernels.
  - Visualized nonlinear transformations and compared the kernel results to linear PCA, especially on data that is not linearly separable.
  - Demonstrated that for nonlinearly separable data, the **first RBF component** already enables near-complete class separation.

--- 

# A5 – ICA 

### **Overview**  
This assignment focuses on **Independent Component Analysis (ICA)** and compares it to **Principal Component Analysis (PCA)** through both theoretical and practical experiments. 

### **Key Tasks**

- **Moment and Cumulant Analysis**  
  - Derived the first four cumulants of a random variable using the Taylor expansion of the cumulant generating function \( K_X(t) = \log \mathbb{E}[e^{tX}] \), and verified moment relations for a standard normal variable using integration tricks and recurrence.

- **Comparison of PCA and ICA on CIFAR-10**  
  - Applied PCA and ICA (via `sklearn.decomposition`) to the CIFAR-10 dataset using 100 components each.  
  - Visualized the extracted components using custom plotting functions.

- **Cocktail Party Problem with FastICA**  
  - Loaded three mono audio signals (`birds.wav`, `ocean.wav`, `frogs.wav`) and mixed them using a random **3×3 full-rank matrix**.
  - Used `FastICA` to blindly recover the original sources from the mixtures.

--- 


# A6 – Factor Analysis

### **Overview**

This assignment focuses on **Factor Analysis (FA)**, 
The task involved deriving and implementing the Expectation-Maximization (EM) algorithm for FA, 
comparing it to a first-order **Gradient Descent (GD)** alternative, and analysing the convergence behavior 
and loss curves.

---

### **Key Tasks**

* **Mathematical Derivation of the EM Algorithm**

  * Implemented the EM procedure for FA based on the lecture derivation:

    * **E-step**: computed $\mathbb{E}[y_i \mid x_i]$ and $\mathbb{E}[y_i y_i^\top \mid x_i]$ using conditional expectations for multivariate Gaussians.
    * **M-step**: derived closed-form updates for the factor loadings $U$ and noise covariance $\Psi$, with matrix speedups applied (e.g., matrix inversion lemma and covariance caching).

* **Efficient Implementation of EM with Speedups**

  * Used the matrix inversion lemma to avoid direct inversion of the full covariance matrix.
  * Replaced sums with precomputed covariance matrices to accelerate batch updates.
  * Vectorized several components (e.g., E-step) for performance and clarity.

* **Comparison of EM and Gradient Descent**

  * Implemented a baseline GD optimization routine for the FA loss function using the analytical gradient of the log-likelihood.
  * Normalized the data to better compare convergence scales across methods.
  * Compared the learning dynamics by plotting loss curves for both EM and GD across multiple random seeds. 

---
