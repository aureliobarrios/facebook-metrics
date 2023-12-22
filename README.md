# facebook-metrics

Evaluating metrics on Facebook posts can be extremely useful for accounts to take into consideration in order to maximize the impact of their posts. Increasing interactions on a post seems to be the goal of every major social media account out there. This project aims to create a machine learning model that analyzes the metrics of a posts in order to get a better understanding of what metrics have a greater impact on the interactions of a post.

## 1. Data

The data used in this project is resourced from the UC Irvine Machine Learning Repository. This dataset contains 500 rows of metrics measured from the posts published by a cosmetics brand during the year of 2014.

> [Facebook Metrics - UC Irvine](https://archive.ics.uci.edu/dataset/368/facebook+metrics)

## 2. Data Wrangling

Although our dataset was fairly clean to begin with there were some extra steps that were needed for the purpose of this project. In this step it was necessary to remove some Null values that were present in the data. We also had to ensure that some of our categorical values made sense in the context they were stored in. In example it was necessary to ensure that columns like `Post Month`, `Post Weekday` and `Post Hour` all had values that made sense. This means that values in the month column were within the range (1 - 12), while weekday had values in the range (1 - 7) and hour had values (1 - 23). Lastly we improved the captions for our column names to make it easier for future analysis.

> [Wrangling Report](https://github.com/aureliobarrios/facebook-metrics/blob/main/notebooks/data_wrangling.ipynb)

## 3. EDA

In our Exploratory Data Analysis stage we found information about our data that can be useful for the next step of modeling. In this analysis we found that there were two instances in our data that were significantly different than the rest of our data. Ultimately deciding to keep these instances in order to capture every instance of the data. We found that our data was sensitive to outliers and that a large majority of our features were strongly correlated to each other. 

> [EDA Report](https://github.com/aureliobarrios/facebook-metrics/blob/main/notebooks/eda.ipynb)

## 4. Modeling

In our final Modeling phase we established a baseline and compared two other models that were implemented using dimensionality reduction techniques. There was an attempt at using Principal Component Analysis to address the multicollinearity within our dataset. The second model used Lasso regression as a form of feature selection to see which features were most useful to our regression model. 

> [Modeling Report](https://github.com/aureliobarrios/facebook-metrics/blob/main/notebooks/model.ipynb)

## 5. Conclusions & Future 

Through our analysis and modeling we found that the features `lifetime_engaged_users` and `lifetime_consumers` were two of the features that were most significant to our target variable. This can provide some insight as to what social media accounts should focus on when creating a post. They should focus on posts that maximize the number of engaged users and the number of consumers. Although we found some insight on important features for the future it would also prove useful to build a model that has more precision on the Mean Absolute Error.
