# Supermarket dataset problem

#### 1) What are interesting business questions? Why are the chosen questions important to be explored?

In the business perspective, we would like to form the question likes **"How can we boost more revenue to supermarket using these transactions data?"** as the goal of the business, in this case supermarket, is to maximize profit as much as possible. So the question should serve the need of the business.

#### 2) What analytics techniques, reports, or dashboards should be used to help solve the selected problems? Please walk us through the process in which you scrutinize the problem. Show us some results or insights.

We apply recommender system to solve the supermarket need. The technique we use is called **"user-based collaborative filtering"** or we recommend the products using the assumption that the customer have the similar behaviour of buying the relevant products. For example, we recommend the bag of ice to customer who buy beer because ,in the past ,most customers are likely to buy the bag of ice with beer.

We generate the vector of product each customer buy and we have to find the most similar vector that fit each customer by finding one with the smallest angle indicating that the pair of customers are likele to buy the same products. The results of implementing the model is shown in the url given above.

#### 3) How data are prepared or processed? Show us an interesting way to transform these data into insights

First, we have to search for the insights of the customers about their behavior. We may group the basket by purchasing hour to see the pattern of purchasing in each day. or we may group the basket by month to see the cycle of purchasing in each year. After we find the hour and the month with the worst performance, we also have to find **buy-less-than-average** customers by segregating customers with spending and time of purchase. Then we compute average spending per purchase for each customers and plot scatter. We generate linear regression in the scatter graph to see which are **buy-less-than-average** customers. And we may pick them to be our target for recommender system.