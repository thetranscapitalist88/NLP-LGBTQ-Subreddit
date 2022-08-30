**Technical Report**

**Problem Statement**:
    Being tasked with the honor to present at the Data Science Conference for 2022. They have asked to touch on two topics, community and NLP Classifiers. So I decided to combine them to ask the question, "As transgender resources for advice increase, how do queer resources change?" The lgbtq+ community is very tech-based and asks for advice online. 

	Therefore the best way to answer this question efficiently is to pull data from two subreddits on the Reddit website using an API "Push Shift." Hence, I have chosen two similar subreddits; r/asktransgender and r/ainbow. The two subreddits seem almost identical, but only further analysis will tell. The similarity will make the models I design challenging. Although, I am up for the challenge. 

**Background**
    It states that for Generational Z, 1 in 6 identifies as queer. As mysterious Gen Z are, they are quickly searching for online communities to help them on their journey of finding themselves. One of their most popular online community is Reddit. A website built for the people to come and talk, ask questions, share their joys or downfalls. Either way, anyone in Reddit has the ability to connect with someone else for advice.

	Then using Natural Language Processing (NPL) models can help me find many insights into how the Reddit community works. Designing NPL Classifier models is very popular in the artificial intelligence (AI) industry. NPL Classifier Models have quick algorithms that predict new data it has never seen before. Relating to the question above, these models I design will help anyone in Reddit make sure they post to the subreddit that best fits their needs. 
    
**Data Dictionary**
|Feature|Type|Dataset|Description|
|---|---|---|---|
|r/asktransgender|object|rainbow_clean df|Subreddit that focuses on transgender advice|
|r/ainbow| object| ask_trans_clean df | Subreddit that focuses on lgbt advice
|combo_clean|object|combo_clean df|Combining the two subreddits to make a full df

**Summary Statistics**
From the data analysis within my notebooks, I have seen that the best NPL Classifier to solve the problem above is the Multinomial Naive Bayes with the Countvectorizer(using stop words) and grid search estimator. This model proved to have an 82% testing score and 83% training score compared to the null model that operated at 51%. Although for the counvectorizer within this model, the max_df & min_df were pushed to their limits, meaning 1 for the max_df and 0 for min_df including the outliers that may have impacted both datasets.

Next, the confusion matrices display demonstrated how well the model predicted. I have tested ten models, and this one was the best. The models have the true positive and true negative above the 1100s. The grid-search Roc Curve Display had a 91% area under the curve. As the models were very similar in nature, the classifier did a great job with its predictions. 

Lastly, when it comes to pulling data, I highly recommend sifting through the data in small chunks before pulling a high amount at one time. For example, the r/ainbow subreddit had over 43% of missing data. This is nearly half the data and can obscure and/or impact my test score. Maybe the model could have been more robust if the data had been filled with actual text? Since I pulled over 6_000 worth of posts, I deleted any missing values within the r/asktransgender subreddit because the NaN's only accounted for around 10%. Cleaning the data was a process, but it did help my model soar above the null value. 

**Recommendations**
1. I recommend that communities who are trying classify similiar topics within their text to use a Multinomial Naive Bayes with a countvectorizer (stop words). Predicting similiar subreddits can be a challenge but this analysis proved it can work. 

2. I recommend that users be careful to limit their title writing to at least 50 characters. Anything after 50, users tend not to respond. The subreddits showed that their can be outliers within online communities. 

3. When pulling data be sure to fully sift through the data to weigh out the options. You can either try to clean it and rreplaced the values with empty strings like I did or you can stop and find a new subreddit. Dealing with 43% or Nan's and "removed", will not help your models.

**Conclusions**
To answer the question above, queer resources will increase just as transgender resources increase. I am worried about all the omitted text, deleted posts, and removed posts from the r/ainbow subreddit. Lastly, NLP models can do incredible work when making binary decisions. My design achieved 83% on two very similar subreddits. 

**Sources**
https://www.reddit.com/r/ainbow/
https://www.reddit.com/r/asktransgender/
https://www.washingtonpost.com/dc-md-va/2021/02/24/gen-z-lgbt/