![LR](https://github.com/fbrowther/Unsupervised-Machine-Learning---Predicting-Myopia/blob/main/Images/d076583b-ecf3-478c-b97e-adcd080985da.jpeg)

# Unsupervised-Machine-Learning to Predict-Myopia

## Brief Introduction - 
Data collected as part of the 'Orinda Longitudinal Study of Myopia' at US National Eye Institute was obtained to determine whether Myopia can be predicted using unsupervised machine learning models. This data is from children aged between 5-9 years old. 
The dataset contained information on Age, measurements taken at opticians (SPHEQ,	AL,	ACD,	LT,	VCD, DIOPTERHR), time children spent on different activities (SPORTHR,	READHR, COMPHR, STUDYHR, TVHR) and whether child's parents had myopia themselves (MOMMY, DADMY).	

## Aims and Objective -
To build Unsupervised Machine Learning that can categorize Myopic children (value =1) from those who do not have Myopia (0) in the age group of 5-9 years old.

## ML Steps to be executed -

      (1) Data Preparation and Scaling,
      
      (2) Dimensionality Reduction using PCA and t-SNE,
      
      (3) Cluster Analysis using KMeans Clustering,
      
      (4) Hyperparameter Tuning to improve the Model,
      
      (5) Hierarchial Clustering to confirm the results,
      
      (6) Making recommendation to the end-users
      
## Specific Libraries and modules employed -
      
      Scikit-Learn ML and Library-
      
            (a) Preprocessing - StandardScaler, normalize
  
            (b) Decomposition - PCA, 
  
            (c) Manifold - TSNE
  
            (d) Cluster - KMeans, AgglomerativeClustering
  
      Scipy.cluster.hierarchy-
      
            (a) dendrogram, linkage
            
## Model Performance -

(1) Dimensionality Reduction (t-SNE_features plot)

![DR](https://github.com/fbrowther/Unsupervised-Machine-Learning---Predicting-Myopia/blob/main/Images/tSNE.png)

The dimentionality of the dataset was reduced using PCA and t-SNE methods. In order to instantiate the PCA model, n_components=0.90 was specified which retained 90% explained variance. However it did reduce the features from 14 to 10. This dimentionality was further reduced using t-SNE analysis (employing the PCA_features). However, this step did not result in any distinguishable clusters that can be further refined to predict if Myopia was present or not.

(2) Kmeans and Elbow Curve 

![EC](https://github.com/fbrowther/Unsupervised-Machine-Learning---Predicting-Myopia/blob/main/Images/Elbow.png)

Kmeans Clustering was carried out on a number of possible clusters (ranging from 1-10) to determine which n_clusters would allow for the inertia to flatten. The elbow curve showed that n_clusters = 3 would be a good number to retrain the data. However this also failed to identify (distinguishable) clusters within the dataset.

(3) Hyperparameter tuning using Initialization (KMeans++ and Random)
Hyperparameter tuning was attempted using initialization and this analysis retured the value of inertia that was only able to identify "single" cluster.

(4) Hierarchial Clustering 

![HC](https://github.com/fbrowther/Unsupervised-Machine-Learning---Predicting-Myopia/blob/main/Images/HClustering.png)

Finally, the dataset was fed through the Hierarchial clustering model to confirm that this dataset infact was clearly indistinguishable employing unsupervised ML models. However, the dataset readily separated into two major clusters (orange and green) most likely indicating myopic and non-myopic children respectivly. The value counts for lables - non-myopic (0)  and myopic children (1) were 537 and 81 respectively.

This indicates that Hierarchial Clustering model can be employed after further refinement to predict presence or absense of myopia in children. 

## Discussion and Conclusions -

           (1) Inspite of performing dimensionality reduction employing PCA and tSNE, no specific pattern or clusters within the dataset was obtained. 

           (2) Furthermore, with the help of the elbow curve the dataset was further analysed employing n_clusters=3; this yielded 
               a inertia value of 6030. Further training of the data specifically using n_clusters=3; didnot yield a successful 
               dispersion of the dataset forming any specific clusters.

            (3) For the unsupervised K-Means algorithm, inertia value can be used to find better hyperparameters. One such method is the 
                initialization.Using Scikit Learn's "k-means++" and "random" methods, the model was re-trained and the value of its inertia 
                was compared. The lower most value of inertia obtained can then be used for hyperparameter tuning. 
                However, in the above dataset, even this approach failed to obtain distinguishable clusters. 

            (4) The dataset was separated into two major clusters (orange and green) (most probably indicating myopic and non-myopic group 
                respectivly) was confirmed by Hierarchial Clustering Model.

            (5) Therefore, it can be concluded that unsupervised Machine Learning algorithm using KMeans (combined with PCA & tSNE) failed 
                to identify any clusters that can be used to predict Myopia in Children aged between 5-9 years old. 
                However, Hierarchial clustering with further refinement of hyperparameters could potentially yield a better performing 
                predictive model.


## Limitations - 

      (1) In the PCA analysis, 90% of the features were retained not allowing the PCA to identify the most contributing features for this dataset. 
      Therefore, the analyses can be repeated with reduced features and assess its performance.
      
      (2) Feature extraction or feature engineering steps can be adopted to combine/improve the features that are being used to build the model.
          

## Data Source: 
Reduced dataset from Orinda Longitudinal Study of Myopia conducted by the US National Eye Institute

