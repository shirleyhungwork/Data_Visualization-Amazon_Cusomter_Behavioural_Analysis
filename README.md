# Exploratory Data Analysis using Tableau: Customer Behaviour in Amazon

Amazon has been one of the world's largest and most influential e-commerce and technology companies, offering a vast range of products through its online platform. Its Prime membership service, offering fast shipping, streaming services, and other benefits, remained popular among consumers, and thus has attracted lots of retail sellers worldwide to join the community. Hence, it would be crucial for merchants to understand customers' behaviour in Amazon, so that they could design better marketing strategy to stand out in such intense competition.

## Data Preprocessing

A dataset has been collected from <a href="https://www.kaggle.com/datasets/swathiunnikrishnan/amazon-consumer-behaviour-dataset">Kaggle</a> from 4th Jun 2023 to 16th Jun 2023. According to the screenshot below, there are 602 data and 23 attributes describing preferences and shopping behaviour in Amazon.
<img src="img/data_preprocess_1.png" loading="lazy" alt="" id="ember1411" class="ivm-view-attr__img--centered  reader-image-block__img evi-image lazy-image ember-view">

As it is observed that customers have answered multiple product categories that they have bought, we have performed data transformation to split it into separate rows. As a result, there are total of 1158 rows in total.
<img src="img/data_preprocess_2.png" loading="lazy" alt="" id="ember1411" class="ivm-view-attr__img--centered  reader-image-block__img evi-image lazy-image ember-view">

In addition, ordinal variables (i.e. Purchase_Frequency) have been assigned to integers with Python code example as show below.
<img src="img/data_preprocess_3.png" loading="lazy" alt="" id="ember1411" class="ivm-view-attr__img--centered  reader-image-block__img evi-image lazy-image ember-view">

Meanwhile, it is found that there are 5 rows having missing values in column "Product_Search_Method" and 1 row having missing value for columns "Service_Appreciation" and "Improvement_Areas". As there are only 6 out of 1158 samples having missing values and there is no specific pattern observed to the missing data, we will ignore the corresponding records in this case.
<img src="img/data_preprocess_4.png" loading="lazy" alt="" id="ember1411" class="ivm-view-attr__img--centered  reader-image-block__img evi-image lazy-image ember-view">

## Exploratory Data Analysis

### Numerical Features

The analysis is started by studying the correlation among numerical features. In accordance to the correlation matrix as shown below, it is found that there is positive correlation between having helpful information from other customers' reviews and possibility of customers adding products to their cart while browsing on Amazon. Below would be the correlation matrix among numerical variables in Tableau:
<img src="https://media.licdn.com/dms/image/D5612AQGkpeG3fQUz8g/article-inline_image-shrink_1500_2232/0/1693538053896?e=1699488000&amp;v=beta&amp;t=bW7n9JybS7KR7zXLgVj4P5kDq4NAsIzHGHmlvTkEBD4" loading="lazy" alt="" id="ember1410" class="ivm-view-attr__img--centered  reader-image-block__img evi-image lazy-image ember-view">

Also, it is shown that customers might purchase more frequently in Amazon if they browse Amazon's website or app more often.

### Categorical Features

As depicted in the following charts, the predominant gender among Amazon customers is female, comprising 57.12% of the samples collected.
<img src="https://media.licdn.com/dms/image/D5612AQGlGvYPB5xBLQ/article-inline_image-shrink_1500_2232/0/1693584373685?e=1699488000&amp;v=beta&amp;t=zytinebqhRjY-wcld387haeUfQMIf_09ljurZCSQCVs" loading="lazy" alt="" id="ember1411" class="ivm-view-attr__img--centered  reader-image-block__img evi-image lazy-image ember-view">

Also, in the box-plot below, it appears that female customers in Amazon generally is the youngest among all with median of 26 years old, whereas male would be the oldest with median of 31 years old. And age is widely distributed for each gender type especially for those that prefer not to specify gender with standard deviation of 11.
<img src="https://media.licdn.com/dms/image/D5612AQEuWeaoKXrEsA/article-inline_image-shrink_1500_2232/0/1693593563064?e=1699488000&amp;v=beta&amp;t=7F53tglvxPM5QutjLExjrB8qbJNgAw6BUnAL82GET88" loading="lazy" alt="" id="ember1412" class="ivm-view-attr__img--centered  reader-image-block__img evi-image lazy-image ember-view">

In the grouped bar-chart below, it shows that keyword search has been popular across all genders, which indicates that it would be essential for merchants to input appropriate keyword so as to increase the chance selling their products.
<img src="https://media.licdn.com/dms/image/D5612AQHT8ZKsdbcUFA/article-inline_image-shrink_1000_1488/0/1693582090127?e=1699488000&amp;v=beta&amp;t=8tZ7hFLGaoeHLfazHZesJltuTHmz3pC97jNY5OPGh5Y" loading="lazy" alt="" id="ember1413" class="ivm-view-attr__img--centered  reader-image-block__img evi-image lazy-image ember-view">

### Dashboard of Visualization in Tableau

Data visualization plays a pivotal role in the realm of data analysis, serving as a cornerstone for effectively conveying information. Presenting data in a comprehensible and visually engaging manner has perennially held great significance. Knowing that Tableau has been a powerful and popular tool in performing data visualization, dashboard is created to visualize customer demographics for each product category that the sellers are interested in with example as shown below.
<img src="https://media.licdn.com/dms/image/D5612AQEYtUtZruj0yA/article-inline_image-shrink_1000_1488/0/1693596346965?e=1699488000&amp;v=beta&amp;t=MWSgId3bL3dfrNes8jymwhhyxX2idNLeitp8qHuNFCA" loading="lazy" alt="" id="ember1414" class="ivm-view-attr__img--centered  reader-image-block__img evi-image lazy-image ember-view">

## Conclusion

Understanding customer demographics is crucial for retailers to have better business planning. Exploratory data analysis using Tableau has provided valuable insights into customer behavior. We have gained a deeper understanding of customer preferences, trends, and patterns as listed below:
- Customers on Amazon are more likely to add products to their cart while browsing when they encounter helpful information in other customers' reviews
- Majority of Amazon customers are female, making up 57.12% of the collected samples with median age of 26.
- Keyword search is widely used by individuals of all genders, highlighting its importance for merchants who aim to boost their product sales.

This analysis has set the foundation for further investigations and model development, including the potential creation of regression or machine learning models to predict customer behaviors more accurately. Overall, the data-driven insights obtained through Tableau will play a crucial role in shaping our strategies and enhancing the customer experience, ultimately leading to improved business outcomes and customer satisfaction.
