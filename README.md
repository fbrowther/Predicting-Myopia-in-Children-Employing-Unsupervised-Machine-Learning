![LR](https://github.com/fbrowther/Unsupervised-Machine-Learning---Predicting-Myopia/blob/main/Images/d076583b-ecf3-478c-b97e-adcd080985da.jpeg)

# Unsupervised-Machine-Learning to Predict-Myopia

## Brief Introduction - 
Data collected as part of the 'Orinda Longitudinal Study of Myopia' at US National Eye Institute was obtained to determine whether Myopia can be predicted using unsupervised machine learning models. This data is from children aged between 5-9 years old. 
The dataset contained information on Age, measuremnets taken at opticians (SPHEQ,	AL,	ACD,	LT,	VCD, DIOPTERHR), time children spent on different activities (SPORTHR,	READHR,	COMPHR,	STUDYHR,	TVHR) and whether child's parents had myopia themselves (MOMMY	DADMY).	

## Aims and Objective -
To build Unsupervised Machine Learning that can categorize Myopic children (value =1) from those who do not have Myopia (0) in the age group of 5-9 years old.

## ML Steps to be executed -
      (1) Data Preparation and Scaling,
      
      (2) Dimensionality Reduction using PCA and t-SNE,
      
      (3) Performing Cluster Analysis using KMeans Clustering,
      
      (4) Hyperparameter Tuning to improve the Model,
      
      (5) Hierarchial Clustering to confirm the results
      
      (6) Make recommendation to the end-users
      
## Specific Libraries and modules employed -
      
      Scikit-Learn ML and Library-
      
            (a) Preprocessing - StandardScaler, normalize
  
            (b) Decomposition - PCA, 
  
            (c) Manifold - TSNE
  
            (d) Cluster - KMeans, AgglomerativeClustering
  
      Scipy.cluster.hierarchy-
      
            (a) dendrogram, linkage
            
## Model Performance -

(1) Dimensionality Reduction
![DR](https://github.com/fbrowther/Unsupervised-Machine-Learning---Predicting-Myopia/blob/main/Images/tSNE.png)

The dimentionality of the dataset was reduced using PCA and t-SNE methods. In order to instantiate the PCA model, n_components=0.99 was specified which retained the 99% of the features for the model. However it reduced the features from 14 to 12. This dimentionality was further reduced using T-SNE on the PCA_features. However, this did not result any distinguishable clusters that can be further refined.

(2) Kmeans and Elbow Curve 
![EC](https://github.com/fbrowther/Unsupervised-Machine-Learning---Predicting-Myopia/blob/main/Images/Elbow.png)


(3) Hyperparameter tuning using Initialization (KMeans++ and Random)


(4) Hierarchial Clustering 
![HC](https://github.com/fbrowther/Unsupervised-Machine-Learning---Predicting-Myopia/blob/main/Images/HClustering.png)

## Discussion and Conclusions -


  








      





## Dataset: 
Reduced dataset from Orinda Longitudinal Study of Myopia conducted by the US National Eye Institute
