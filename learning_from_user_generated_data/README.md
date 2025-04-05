# Exercise 1: RecSys Basics I

### **Overview**
This assignment explores **recommender systems**, focusing on interaction-based filtering and popularity-based recommendations using music (LFM-2B) and movie (MovieLens-1M) datasets.

### **Key Tasks**

- **Interaction Matrix**  
  - Constructed a binary user-item interaction matrix based on implicit feedback.
  - Applied a thresholding mechanism to filter out insignificant interactions.

- **Popularity-Based Recommendations**  
  - Implemented a baseline recommender that suggests the most popular unseen items.
  - Ensured efficient ranking and exclusion of previously consumed content.
  - Extended the popularity-based approach to recommend items based on regional preferences.

---

# Exercise 2: Collaborative Filtering + Implicit Feedback

### **Overview**
This assignment builds on recommender system fundamentals by implementing an **item-based collaborative filtering** approach using implicit user-item interactions from the LFM-Tiny dataset.

### **Key Tasks**

- **Item Similarity Calculation**  
  - Implemented Jaccard similarity to compare item interaction vectors.
  - Calculated similarity scores between items using a modular and reusable similarity engine.

- **User-Item Scoring**  
  - Predicted user preferences by averaging top-N similarities between the target item and items previously consumed by the user.
  - Ensured exclusion of the target user from similarity computation to avoid bias.

- **Top-K Recommendation System**  
  - Built an efficient recommender that ranks unseen items based on predicted user-item scores.
  - Returned top-k personalized recommendations with corresponding similarity scores.

---

# Exercise 3: Model-Based approaches

### **Overview**
This assignment introduces **model-based collaborative filtering** using **matrix factorization techniques** to generate personalized item recommendations based on implicit feedback from the LFM-Tiny dataset.

### **Key Tasks**

- **Matrix Factorization via SVD**  
  - Implemented truncated Singular Value Decomposition (SVD) to extract compact latent representations of users and items.
  - Used dot product of latent vectors to approximate interaction scores and generate recommendations.

- **Iterative Matrix Factorization with PyTorch**  
  - Built a trainable matrix factorization model using `nn.Embedding` layers for user and item embeddings.
  - Trained the model using binary cross-entropy loss and the Adam optimizer, reconstructing the full user-item interaction matrix.

- **Top-K Recommendation Engine**  
  - Developed a recommendation function that ranks unseen items based on dot-product similarity between user and item embeddings.
  - Ensured exclusion of previously interacted items and padded the result with `-1` if fewer than `topK` items were available.

---
