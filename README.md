# Womens_Ecommerce_Reviews

This is a Women’s Clothing E-Commerce dataset revolving around the reviews written by customers. Its nine supportive features offer a great environment to parse out the text through its multiple dimensions. Because this is real commercial data, it has been anonymized, and references to the company in the review text and body have been replaced with “retailer”.

# Context

This dataset includes 23,486 rows and 10 feature variables. Each row corresponds to a customer review, and includes the variables:

* Clothing ID: Integer Categorical variable that refers to the specific piece being reviewed.
* Age: Positive Integer variable of the reviewers age.
* Title: String variable for the title of the review.
* Review Text: String variable for the review body.
* Rating: Positive Ordinal Integer variable for the product score granted by the customer from 1 Worst, to 5 Best.
* Recommended IND: Binary variable stating where the customer recommends the product where 1 is recommended, 0 is not recommended.
* Positive Feedback Count: Positive Integer documenting the number of other customers who found this review positive.
* Division Name: Categorical name of the product high level division.
* Department Name: Categorical name of the product department name.
* Class Name: Categorical name of the product class name.'

In this project, I chose linear and logistical regression. With the text of the reviews being present, I also decided to try NLP to see how accurate a model could be in predicting the rating based off the sentiment of the text.

# The Code
Import these libraries to start for exploratory data analysis

![capture1](https://user-images.githubusercontent.com/33237727/44468577-831aae80-a5f3-11e8-95f5-2a31baa01d6d.PNG)

And the head of the data frame

![capture2](https://user-images.githubusercontent.com/33237727/44468652-b4937a00-a5f3-11e8-9856-35f0dd436b07.PNG)

![capture3](https://user-images.githubusercontent.com/33237727/44468746-ec9abd00-a5f3-11e8-8301-a6ec5aaee27a.PNG)


## My first question was attempting to predict the rating based on the type of clothing:

This was done using a linear regression model through Scikit-Learn

![capture4](https://user-images.githubusercontent.com/33237727/44468932-5d41d980-a5f4-11e8-966d-515e03bddda4.PNG)

Due to the results of the training and test scores, I decided to move on to logistic regression to using two different features.

## Logistic Regression

Scores ended up being 26% between the training and testing data. Although, that is better than what we have above, now is the time to see if Natural Language Processing can help with our predictions. 

## NLP Portion

First is to obtain the text length. I added another column specifically for this.

![capture6](https://user-images.githubusercontent.com/33237727/44470551-0807c700-a5f8-11e8-9835-eb4bd7cc08cd.PNG)


I then explored the data using matplotlib for a bit of a bird's eye view.

![capture7](https://user-images.githubusercontent.com/33237727/44470818-a300a100-a5f8-11e8-9f8b-eef76e2f0e58.PNG)


The results ended up coming out as 27% and the model was only correct that amount of time.
