# Amazon_Vine_Analysis
Analysis of Amazon Reviews with PySpark, Pandas and SQL
## Overview of the Analysis:

Online shopping often heavily relies upon reviews of product to help persuade customers into purchasing a particular product.  As one would expect, product with more positive reviews will most likely outperform a product with less positive reveiws or even more negative reviews.  When shopping online it is important to consider not only a products rating but also the number of reviews used to determine the rating (a product with a five star rating and 100 reveiws vs. a product with a 4 star rating and over one thousand reviews).  

In addition to this, there are companies that offer paid reviews for product where a reviewer is provided a product and they are required to write a published review.  One such program is the Amazon Vine program.  If a company chooses to participate in this program they pay a fee to Amazon and then their product is provided to members of the Vine program for reviews.  For this particular analysis reviews for video games sold on Amazon we analyzed to compare the number of five star reviews for paid and unpaid reviews.  

## Results:

After the video game reviews dataset was cleaned up, 4 separate dataframes were created: reviews, customers, products, and vine reviews.  These dataframes were then placed into SQL tables via an AWS RDS and Google Colab notebook using PySpark.  Once in pgAdmin, the vine reviews table was exported as a CSV and further transformed with Pandas to provide the results below:

* How many Vine reviews and non-Vine reviews were there?

    - ![Number of Vine reviews](https://github.com/matthewdouglasmartin/Amazon_Vine_Analysis/blob/main/Resources/Number_of_Vine_Reviews.png)

    - ![Number of non-Vine reviews](https://github.com/matthewdouglasmartin/Amazon_Vine_Analysis/blob/main/Resources/Number_of_nonVine_reviews.png)

* How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

    - ![Number of Vine 5 star reviews](https://github.com/matthewdouglasmartin/Amazon_Vine_Analysis/blob/main/Resources/Nunber_paid_5star.png)

    - ![Number of non-Vine 5 star reviews](https://github.com/matthewdouglasmartin/Amazon_Vine_Analysis/blob/main/Resources/Number_unpaid_5star.png)

* What percentage of Vine reviews were 5 stars? What percentage of non-vine reviews were 5 stars?

    - ![Percentage of 5 star Vine Reviews](https://github.com/matthewdouglasmartin/Amazon_Vine_Analysis/blob/main/Resources/Percent_paid_5star.png)

    - ![Percentage of 5 star non-Vine reviews](https://github.com/matthewdouglasmartin/Amazon_Vine_Analysis/blob/main/Resources/Percent_unpaid_5star.png)

## Summary:

Based off of the results above, 51.1% of paid reviews are 5 stars while 38.7% of unpaid reviews are 5 stars. Thus it is more likely for a paid reviewer to give a 5 star review than it is for an unpaid (exhibiting positiviy bias).  One additional analysis that would help to further support this conclusion would be to take it one step further and compare 4 star reviews and 1 star reviews.