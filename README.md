# Movie-Recomender-Movielens-Dataset-

Using Movielens small dataset(with 1,00,000 ratings)
Language: Pyhton (With Pandas, numpy, scikit)

I am building a recommendation engine which recommends movies. We do it by calculating similarity between the users and suggesting movies which similar users (minimal distance to user to whom we should recommend) and pick 5 movies movies based on their previous ratings. I have also compared it with KNN clustering algorithm by taking RMSE as measurement metric. I am using pearson coefficient to calculate similarity between users, which is used for recommending.

As our is not to just predict the rating, but given a unseen movie we should be able to tell whether he/she likes it or not(gives a 3.5+ rating). So I have also divided ratings into class and calculated RMSE. 
After calculating similarities for recommending to a particular usedid we filter users(users with similarity above than threshold value) get a movie list which [s]he hasn't watched but similar users did. For each user, We calculate product of their respective similarity and rating and get average of this product for each movie and recommend the highest product value movies.