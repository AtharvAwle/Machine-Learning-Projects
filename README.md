# 🎬 Movie Recommendation System

##  Project Overview
This project is a **content based movie recommendation system** built using the TMDB movie dataset. It recommends movies based on similarity in content such as genres,keywords,overview,cast and crew.

## 📂 Dataset Used
- https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

## ⚙️ Approach
The dataset consisted of two files movies and credits which I merged into a single dataset using titles.After merging all columns were analysed and only the relevant ones required for content based tagging were kept (genere,overview,keywords,cast and crew).The data was cleaned by removing duplicate rows and NaN values.As few columns were stored in dictionary format they were converted into lists and then the white spaces were removed.Once the data was prepared each movie was vectorised using scikit learn CountVectorizer function.As many words appeared repeatedly stemming was applied to reduce them to their main original root form.All selected features were then combined into a single column called 'tags'.Then to calculate similarity between movies cosine similarity was used instead of euclidean distance as it performs better for text based data.Finally after having similaroty score a recommend function was implemented which takes a movie name as input identifies its index sorts the similarity scores in descending order and returns the top 5 most similar movie titles using iloc.
