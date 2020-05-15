Module 4 project: Recommendation System

Business problem.

We have been asked to build a model that provides top 5 movie recommendations to a user, based on their ratings of other movies. The dataset that we are using to build our model is the "small" MovieLens dataset containing 100,000 user ratings from the GroupLens research lab at the University of Minnesota. 

Implementation.

By appreciating that there is a cold start issue the goal is to overcome this problem and beeing able to provide recommendations to users with small past history. In order to do that we designed an hybrid model using singular value decomposition (SVD) as a primary model and item to item as a secondary model. We used a Python library called Surprise, an easy-to-use Python scikit for recommender systems. 

Evaluation.

We evaluated the model by using tre different metrics: the Root Mean Square Error(RMSE), the Normalized Discounted Cumulative Gain(NDCG) and the Mean Absolute Error(MAE).

Conclusion.

Our hybrid model overcame the cold start problem by at first recommending 5 of the 50 most popular movies if the user had rated less than 5 movies on his account. Following that we used our secondary item to item model until the user has rated 15 movies, after which the primary SVD model is used. 