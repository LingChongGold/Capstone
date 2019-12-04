# Problem Statement
**Business Problem:**<br>
Analyse and understand the customers and recommend actions to increase sales volume

**Data Science Problem:**<br>
- Perform Analysis on product and customer purchase behavior to gather insights 
- Perform Basket Analysis
- Create a recommender system with the absence of explicit feedback and customer demographic profile

# Executive Summary

In this project, we performed data manipulation and data visualisation using Pandas, Numpy and Matplotlib, then performed an analysis on customer's purchase behaviour to derive at insghts for business actions. 

Customer segmentation based on the products they frequently purchased was performed through unsupervised learning, and another round of analysis was performed on the clusters to understand the unique characteristics of each clusters. Marketing and promotional recommendations were made targetting at the respective clusters for better effectiveness and customer satisfaction. Association rule mining was performed using Apyori library and a collaborative filtering recommender system with implicit feedback was built using Implicit library.

Gathered data was split into 6 csv files, and they contain past purchases of customers and product details. Source of the data can be found at [Kaggle](https://www.kaggle.com/c/instacart-market-basket-analysis).

### Data Analysis

From our detailed data analysis, we concluded and recommended the following:<br><br>
__Top Product Category__<br>
Perishables, Organic and Fruits are the top sellers for the organisation. This makes sense as due to their shorter shelf live, they needs to be replenished more often. 

__Order Size and Reorder Rate__<br>
Most clients purchase between 3 to 10 products in a single order. The first 10 products added to cart are more likely to be reordered again and the quantity of products sold is highly influenced by their re-order rate.

__Strategic Time for Campaigns and Flash Deals__<br>
Mondays between 9AM to 11AM and Sundays between 9AM to 5PM are peak period when most orders are made, these are the best time for marketing campaigns or flash deals as we will have maximum outreach.

There are no orders coming in between 1AM to 5AM, these are the best time for system maintenance or upgrading.

__Strategic Push Notification__<br>
Most of the customers performs weekly or monthly grocery shopping, we can schedule our push notification strategically to encourage purchases. 

__Customer Retention__<br>
It is noticed that the organisation have a small group of loyal customer who had made 99 purchased, however it is also noticed that the organisation is not able to retain the customers effectively.<br><br>
The organisation can look into ways to increase customer retention or look into what could have caused the customers to churn. The organisation can do so by finding out what was done well from the group of loyal customers and reach out to new customers after their fourth order to gather feedback and let the customer's voices be heard.

### Customer Segmentation

Customers are segmented into 3 different groups based on the sub-category of products they purchase.

__Cluster 0 (Convenience)__<br>
This cluster has the most number of customers at 183151, and the average order per customer is 11.5. We can infer that this segment of customers holds the most one time off customer.<br><br>
The top sub-categories of product purchased includes frozen meals, soft drinks and packaged produce. We can infer that this cluster of customer prefers convenience and may have litle or no time to prepare their meals from scratch. They cold be from families consisting of working class or young adults who may have limited expertise in preparing meals.<br><br>
Promotional items related related to snacks, ready to eat meals or equipment which enable fast and convenient meal preparation can be targeted at this cluster. We can also consider having easy to prepare recipes with fresh products from the store targeting at this cluster of customer. This will increase product interaction for this cluster of customer, and possibly move them to the fresh cluster, increasing diversity to our customer base and at teh same time retain them.

__Cluster 1 (Fresh)__<br>
This cluster has 21278 customers, and the average order per customer is 47.6. We can infer that this segment of customer are people with time and expertise in preparing more advance meals and they like their items fresh.The absence of ready-to-eat meals and fresh items are amongst the top purchases for this segment of customers.<br><br>
Membership perks like free fixed routine delivery should they commit to a certain amount of orders in a week. With such membership perks, we can improve customer loyalty and retention.

__Cluster 2 (Babies)__<br>
This cluster has 1780 customers , and the average order per customer is 45. The most distinct purchase of this segment is the high purchase count of baby food formula.<br><br>
Baby related promotions or products can be targeted at this segment of customers and we can also consider providing infant care tips with products from our store for this segment of customer to prepare them for their next stage of parenthood.

### Basket Analysis
Basket analysis captures patterns appearing frequently together and can be used to recommend items when a customer add an item to their cart. Frequently bought together items can be placed near to each other in brick and mortar shop to improve customer experience when shopping. Other use cases related to this analysis is that the organisation can study the association and consider bringing in new products.<br>

From our analysis through the available data, we uncovered 421 association rules. An interesting discovery is that organic strawberries and organic reduced fat milk are frequently bought together. The organisation can consider introducing Organic Reduced Fat Milk in strawberry flavour to the store based on this and determine the take up rate.

### Improve Sales (Recommender System)

With the gaining traction of data privacy, it is foreseen that there will be more challenges ahead in gathering customer's identifiable or possibly demorgraphic profile. Explicit feedbacks like ratings and reviews tends to be skewed towards some level of biasness depending on the circumstances leading to how the rating or feedback was given and difference in expectations of individuals.<br>

According to studies, 75% of what Netflix consumers watch comes from the company's recommender system and Amazon credit 35% of their revenue to their reccomender system. A reccomender system enables the organisation bring awareness to consumers on products which they do not have interaction before as they may not be aware of the existence of the product.<br>

With these in mind, it is determined that a good way to boost sales is by building a recommender system based on implicit feedbacks derived from the purchase history of the customers.<br>

A validation dataset was prepared containing purchases of a customer's last order which was not seen by our model, with the other preceding orders, our model will perform recommendations on products which the customer have not interacted before. A sample of 5 customers was chosen and the recommendation evaluated.

__Customer 1__<br>
Customer bought Milk Chocolate Almonds in the validation dataset and one of the product our recommender system recommended is Hazel Nuts in Milk Chocolate.<br><br>
In this instance, our recommender system recommended two kind of bread twice, which can be better improved for more diversity in the recommendatons

__Customer 3754__<br>
Customer bought Skin and Haircare product in the validation dataset and one of the product our recommender system recommended is Shampoo.

__Customer 58144__<br>
Customer bought banana and Raspberry Yoghurt in the validation dataset and one of the product our recommender system recommended is Medium Scarlet Raspberries

__Customer 114401__<br>
Customer bought a variety of fruit juices and one of the product our recommender system recommended is Coconut and Pineapple Juice

__Customer 200372__<br>
There are no recommendations which are closed to what the customer purchased in the validation set<br>

a deeper dive into the past purchase of the customer uncovered that the customer had purchased a variety of bread spreads and supplments in the previous orders, and 2 of the products our recommender system recommended is MCT oil which is a supplement of weight loss and energy for exercising and Ghee Vanilla Bean which is butter for spreading bread.

### Next Steps and Future Improvements
Deploy the recommender system and evaluate the effectiveness based on the take up rate of recommended items and study the result for improvements for the next iteration.<br>

Add features tags to the products like organic, natural, convenient, fresh, price range, manufacturer for the next iteration of improvement.<br>

Use neural networks, Sequential to predict customer's next purchase and perform association rules for new recommendations.<br>

Additional analysis can be performed on the customer with more data to gain insights on additional segments based on their recency of their last purchase, frequency of order, amount spent in the store.<br>