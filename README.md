# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Choose the number of clusters (K).

2.Randomly initialize K centroids.

3.Assign each data point to the nearest centroid.

4.Recalculate the centroids.

5.Repeat steps 3 and 4 until centroids do not change. 

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: E ARYA KRISHNA 
RegisterNumber: 212225240014 
*/
```
```
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
data = pd.read_csv("Mall_Customer.csv")
X = data.iloc[:, [3, 4]].values
kmeans = KMeans(n_clusters=5, random_state=0)
y_kmeans = kmeans.fit_predict(X)
plt.scatter(X[:, 0], X[:, 1], c=y_kmeans, s=50)
plt.scatter(kmeans.cluster_centers_[:, 0],
            kmeans.cluster_centers_[:, 1],
            s=200,
            marker='X')
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("Customer Segmentation using K-Means")
plt.show()
```

## Output:
<img width="645" height="390" alt="Screenshot 2026-05-16 085619" src="https://github.com/user-attachments/assets/3e47dd01-e376-4f44-8d6a-718db80b05c3" />
<img width="791" height="566" alt="Screenshot 2026-05-16 085636" src="https://github.com/user-attachments/assets/8807b59e-47a8-46b2-b668-2ebcc3272927" />




## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
