## Anime Recommendation System

![image](https://github.com/abhaymishra24/Anime-recommend-module/blob/main/anime_banner.png) 

Anime Recommendation System is a content-based recommendation system that provides personalized anime recommendations based on user preferences. It utilizes a dataset scraped from [Anime Planet](https://www.anime-planet.com/) and employs various techniques such as data cleaning, text preprocessing, and feature extraction to create a content representation for each anime.<br>

Using the content representation of the selected anime, the recommendation system calculates the similarity between the selected anime and other anime in the [dataset](https://github.com/atharv-patil/anime-recommendation-system/blob/main/anime.csv). It then generates a list of the top 5 recommended anime based on their similarity scores.<br>
The recommendation system focuses on leveraging the characteristics and features of individual anime to make recommendations. It does not consider collaborative filtering or user preferences. Instead, it identifies similar anime based on the content attributes such as genres, themes, and descriptions.

## Table of Contents
- [Data Cleaning](#data-cleaning)
- [Text Preprocessing](#text-preprocessing)
- [Feature Extraction](#feature-extraction)
- [Similarity Calculation](#similarity-calculation)
- [Web App](#web-app)
- [Key Learnings](#key-learnings)

## Data Cleaning
The [data](https://github.com/atharv-patil/anime-recommendation-system/blob/main/anime.csv) was cleaned using the NumPy and Pandas libraries. Preprocessing steps, such as handling missing values and removing duplicates, were performed to ensure the data quality. Here is the link of [Jupyter Notebook](https://github.com/atharv-patil/anime-recommendation-system/blob/main/anime-recommender-system.ipynb).

## Text Preprocessing - 
To handle different word tenses and variations, the nltk library's PorterStemmer was used. This helped in standardizing the text data and improving the accuracy of the recommendation system.

## Feature Extraction -
The sklearn.feature_extraction.text module's CountVectorizer was employed to extract relevant features from the text data. It identifies the most frequently used words and creates a matrix representing the frequency of each word in a given row.

## Similarity Calculation - 
Using the cosine_similarity function from sklearn.metrics.pairwise, the similarity between two anime rows was calculated. Since the recommendation system operates in a multidimensional space, cosine similarity is preferred over Euclidean distance. The resulting similarity scores range between 0 and 1.

## Web App - 
The project includes a web app created with the help of the pickle library and Streamlit framework. The serialized data and similarity matrix were loaded using pickle to enable real-time recommendations based on user input.

![image](https://github.com/atharv-patil/anime-recommendation-system/assets/83455141/210c9e52-a98a-478e-98bc-007ea801b886)

https://github.com/atharv-patil/anime-recommendation-system/assets/83455141/151ca033-11b0-4a6d-a51e-0c8f426b9d8a

## Key Learnings
##### Through this project, I gained valuable insights into the following concepts:
- Bag of Words
- CountVectorizer for feature extraction
- Cosine distance and similarity
- Text preprocessing using PorterStemmer