# Movie_Recommendation_Sysytem
MovieLens - 32M

# Content-Based Recommendation
#### Content-based systems analyze the attributes of items (e.g., movies) and recommend items with similar features to the user’s preferences. The system assumes that users will like items that are similar to ones they have already enjoyed.

# Key features used:

#### Genres: Categorical data representing movie genres.
#### Tags: User-generated keywords describing movies.
#### Ratings: Numerical data capturing user ratings for movies.

# Non-KNN Approach
#### This method uses a direct similarity computation between movies:

### a. Feature Extraction
#### Genres: Transformed into a structured format where each genre is treated as a binary feature (present or absent for a movie).
#### Tags: Processed using text vectorization techniques like Term Frequency-Inverse Document Frequency (TF-IDF), which assigns weights to words based on their importance in describing a movie.
### b. Similarity Calculation
Cosine Similarity: Measures the cosine of the angle between two feature vectors. Higher similarity values indicate that two movies are closely related in terms of their features.
### c. Recommendation
#### Find the most similar movies by sorting similarity scores and selecting the top matches.

# KNN-Based Approach
#### This method uses the K-Nearest Neighbors (KNN) algorithm to recommend movies.

### a. Feature Preparation
#### The same features (genres, tags, ratings) are extracted and processed as in the non-KNN approach.
#### Additionally, numerical features like ratings are scaled to ensure uniformity across all features.
### b. KNN Algorithm
#### K-Nearest Neighbors (KNN): An unsupervised learning algorithm that identifies the k closest neighbors to a given movie based on a chosen similarity metric (e.g., cosine distance).
#### The model is trained on the feature matrix, enabling it to quickly find similar movies for a given input.
### c. Recommendation
#### Retrieving the k most similar movies from the trained KNN model.
