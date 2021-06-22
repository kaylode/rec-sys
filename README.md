# :star: **Traditional Recommendation System** :star:

## Code Session
[![Notebook](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SpFhY9uL-RTYnIqkl-NgAYMqbVSlm_kj?usp=sharing)

## **Content-based Recommendation System**
1. Vectorize items using TF-IDF
2. Compute cosine similarity between all items
3. Recommend top most similar items with query item

## **Colaborative Filtering (CF)**
- CF uses only User-Item matrix, require no other item's information.
- CF consist of two types: 
  - Memory-based
  - Model-based

### **Memory-based: Item-based Recommendation**
- To predict rating of user U for item I:
1. Use vector V_ui from User-Item matrix
2. Compute cosine similarity between all V_ui
3. Use k-nearest neighbors V_uj, similar to V_ui
4. Compute predicted score based on ratings of k neighbors

### Model-based: Low-rank approximation using SVD decomposition 
- To predict rating of user U for item I:
1. Use SVD decomposition to factorize User-Item matrix into U, Sigma, V
2. Apply Eckart–Young–Mirsky theorem (Frobenius norm) to get U_k, Sigma_k, V_k
3. Get A_k  = U_k · Sigma_k  · V_k 
4. Use A_k for predicting ratings

## References
- https://en.wikipedia.org/wiki/Low-rank_approximation
- https://github.com/shivam1808/Recommendation-System
- https://www.kaggle.com/prashant111/recommender-systems-in-python
- IMDB Dataset: https://www.kaggle.com/rounakbanik/the-movies-dataset
