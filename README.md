# Machine-Learning-Module 6
Project Name-Netflix movie and TV show Clustering
![Netflex](https://github.com/user-attachments/assets/afb40769-7b61-4d4c-abb3-261a7a9e37e2)
The aim of this project is to analyze the Netflix Dataset of movies and TV shows until 2019, sourced from the third-party search engine Flixable. The goal is to group the content into relevant clusters using NLP techniques to improve the user experience through a recommendation system. This will help prevent subscriber churn for Netflix, which currently has over 220 million subscribers.
Additionally, the dataset will be analyzed to uncover insights and trends in the streaming entertainment industry.

**The project followed a step-by-step process:**

Handling null values in the dataset.
Managing nested columns (director, cast, listed_in, country) for better visualization.
Binning the rating attribute into categories (adult, children's, family-friendly, not rated).
Performing Exploratory Data Analysis (EDA) to gain insights for preventing subscriber churn.
Creating clusters using attributes like director, cast, country, genre, rating, and description. These attributes were tokenized, preprocessed, and vectorized using TF-IDF vectorizer.
Reducing the dimensionality of the dataset using PCA to improve performance.
Employing K-Means Clustering and Agglomerative Hierarchical Clustering algorithms, determining optimal cluster numbers (4 for K-Means, 2 for hierarchical clustering) through various evaluation methods.
Developing a content-based recommender system using cosine similarity matrix to provide personalized recommendations to users and reduce subscriber churn for Netflix.
This comprehensive analysis and recommendation system are expected to enhance user satisfaction, leading to improved retention rates for Netflix.
In the face of an ever-growing library of movies and TV shows, providing tailored and precise movie recommendations has become essential for Netflix to enhance user experience and encourage sustained platform engagement. The challenge is to create an advanced recommendation system capable of accurately predicting user preferences to offer personalized movie recommendations to each user. The primary focus of this project is to design and implement a recommendation system that addresses the following core objectives: Personalized Recommendations: Develop a system capable of producing customised movie suggestions based on user viewing history, behaviour, preferences, and interactions with the platform. User Engagement: Enhance user satisfaction and engagement by presenting recommendations aligned with individual preferences, increasing the likelihood of continued and regular use of the Netflix platform. Content Discovery: Enable users to discover a broader range of movies, ensuring optimal utilization of Netflix's extensive library while increasing viewer engagement.

**Data overview-**
![image](https://github.com/user-attachments/assets/4656e4fa-ee12-4cb7-8000-0f4e382278d1)

**Attribute Information**
show_id: Unique ID for every Movie / TV show
type: Identifier - A Movie or TV Show
title: Title of the Movie / TV show
Director: Director of the Movie
cast: Actors involved in the movie/show
country: The country where the movie/show was produced
date_added: Date it was added on Netflix
release_year: Actual Release year of the movie/show
rating: TV Rating of the movie/show
duration: Total Duration - in minutes or number of seasons
listed_in: Genere
description: The Summary description

**Approach-**
The following steps were followed in the project:

Data Preprocessing: The dataset was preprocessed and cleaned to handle missing values, outliers, and any inconsistencies in the data.
Text data preprocess- Lower Casing, Removing Punctuations, Removing URLs & words containing digits, removing Stopwords & White spaces, rephrasing text, Tokenization, Text Normalization, Part of speech tagging, and Text Vectorization. Dimensionality Reduction(PCA)

Data Clustering: The preprocessed data was clustered in different groups based on similarity and grouped based on the elbow method or silhouette score. By using different clustering algorithms we group similar data.

Model Deployment: The selected model can deployed using pickle, where it could recommend movies based on similarity created in different clustering algorithms. The model's performance can be monitored over time to ensure its usefulness.

**Model Used**

For modelling, we tried various clustering models such as 

1)K-Means Clustering

2)Hierarchical Clustering (Agglomerative Clustering)

3)Silhouette Score for Clustering

4)Elbow method for Clustering

**Result**
From the Elbow method and Silhouette score, we can choose the optimal no of clusters to group data based on the similarity of the data. in the end I use cosine similarity to build a recommendation system which recommends movies based similarity and clusters.

**Output**
![image](https://github.com/user-attachments/assets/e4b88974-fe9f-45e2-8113-5ff70737ef70)
![image](https://github.com/user-attachments/assets/b157ef4e-8506-4ba8-9132-2bd04cbf5f04)
![image](https://github.com/user-attachments/assets/6a4a9109-91bc-4a7e-832a-aa870fcaf288)
![image](https://github.com/user-attachments/assets/008de856-858e-40be-9294-28c7780ddb01)

**Conclusion**

During our analysis, Firstly I cleaned the data and conducted an exploratory data analysis (EDA) on all the features in our dataset. First I analyze my variable applied transformations as per requirement. Then I evaluate categorical variables to implement clustering algorithms. I have done Monovariate and Bivariate analysis on these variables. I also studied the numerical variables, calculated their correlations, and their relationships with the dependent variable.

1)I employed 2 machine learning algorithms including K-Means Clustering, Hierarchical Clustering (Agglomerative Clustering), Silhouette Score and Elbow method to get the optimal no of clusters.

2)Implemented K-Means Clustering and Agglomerative Hierarchical Clustering, to cluster the Netflix Movies TV show dataset.

3)The optimal number of clusters we are getting from K-means is 4, whereas for Agglomerative Hierarchical Clustering the optimal number of clusters are found out to be 2.

4)We chose Silhouette Score as the evaluation metric over distortion score because it provides a more intuitive and interpretable result. Also Silhouette score is less sensitive to the shape of the clusters.

5)Built a Recommendation system that can help Netflix improve user experience and reduce subscriber churn by providing personalized recommendations to users based on their similarity scores.

6)Movies make up about two-thirds *of Netflix content, with TV shows comprising the remaining *one-third.

7)69.1% of the data belongs to movies and 30.9% of the data for TV shows.

