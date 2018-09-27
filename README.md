# recommendation-system
### Dataset: 
The dataset that I’m working with is MovieLens, one of the most common datasets that is available on the internet for building a Recommender System. 
### Types of recommendation syatems i have used:
 - Content Based Recommendation System:
   *  A content based recommender works with data that the user provides, either explicitly movie ratings for the MovieLens dataset.   Based on that data, a user profile is generated, which is then used to make suggestions to the user. As the user provides more inputs or takes actions on the recommendations, the engine becomes more and more accurate.
   * The Math:
    - The concepts of Term Frequency (TF) and Inverse Document Frequency (IDF) are used in information retrieval systems and also   content based filtering mechanisms (such as a content based recommender).
    - After calculating TF-IDF scores, how do we determine which items are closer to each other, rather closer to the user profile? This is accomplished using the Vector Space Model which computes the proximity based on the angle between the vectors.-
    - I will be using the Cosine Similarity to calculate a numeric quantity that denotes the similarity between two movies.
     
   
   
   
 - Collaborative Based Recommendation System:
   * The Collaborative Filtering Recommender is entirely based on the past behavior and not on the context. More specifically, it is based on the similarity in preferences, tastes and choices of two users. It analyses how similar the tastes of one user is to another and makes recommendations on the basis of that.
   * The Math:
     There are 2 main types of memory-based collaborative filtering algorithms:
    - User-User Collaborative Filtering: 
      Here we find look alike users based on similarity and recommend movies which first user’s look-alike has chosen in past. This
    - Item-Item Collaborative Filtering:
      It is quite similar to previous algorithm, but instead of finding user’s look-alike, we try finding movie’s look-alike.
   * There are 3 distance similarity metrics that are usually used in collaborative filtering:
    - Jaccard Similarity: Similarity is based on the number of users which have rated item A and B divided by the number of users who have rated either A or B. It is typically used where we don’t have a numeric rating but just a boolean value like a product being bought or an add being clicked.
    - Cosine Similarity: (as in the Content-Based system) Similarity is the cosine of the angle between the 2 vectors of the item vectors of A and B. Closer the vectors, smaller will be the angle and larger the cosine.
    - Pearson Similarity: Similarity is the pearson coefficient between the two vectors. For the purpose of diversity, I will use Pearson Similarity in this implementation.
   * A well-known matrix factorization method is Singular value decomposition (SVD). At a high level, SVD is an algorithm that decomposes a matrix A into the best lower rank (i.e. smaller/simpler) approximation of the original matrix A. 
   * The Evaluation
     There are many evaluation metrics but one of the most popular metric used to evaluate accuracy of predicted ratings is Root Mean Squared Error (RMSE). I will use the mean_square_error (MSE) function from sklearn, where the RMSE is just the square root of MSE. I get a mean Root Mean Square Error of ***0.8736*** which is pretty good.  
      
 - Hybrid Based Recommendation System:
   
 
 
