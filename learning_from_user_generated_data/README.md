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