# Amazon Reviews K-NN Analysis
This notebook will evaluate polarity of amazon reviews using a K-NN approach.

Following these steps:
1. **Download the dataset** from [Amazon Reviews on Kaggle](https://www.kaggle.com/datasets/kritanjalijain/amazon-reviews?resource=download)  
2. **Dataset Description:**  
   The dataset consists of two CSV files: `train` and `test`, each containing the following fields:  
   - **polarity**: 1 for negative, 2 for positive  
   - **title**: review heading  
   - **text**: review body  

3. **Sparse Vectors Generation:**  
   - Apply **q-shingle** with `q=3` on the training data.

4. **MinHashing & LSH:**  
   - Apply **MinHashing Locality-Sensitive Hashing (LSH)** on the sparse vectors of the training dataset.

5. **K-Nearest Neighbors Classification:**  
   - Use the **test set** and apply **k-nearest neighbors (k=3)** on the hashed training data.  
   - Classify each test instance based on the majority polarity of its `k` nearest neighbors.

6. **Cluster Identification:**  
   - Identify **clusters of reviews** where each pair of reviews has a **similarity greater than 0.6**.  
   - This step should be performed after the introduction to **network analysis**.