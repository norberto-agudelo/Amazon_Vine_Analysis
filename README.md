# Module 17. Big Data Amazon_Vine_Analysis
## Overview 

The purpose of this challenge is to apply some skills and subjects related with big data learned during the week.
We are going to use some cloud services to store store large amounts of data as well as perform an ETL process to analyze some data. We'll use Cloud Databases and Cloud Storage with S3 on Amazon Web Services, the most popular cloud service available.

With this purpose in mind, the goal of the project is to analyze Amazon reviews written by members of the paid Amazon Vine program by using any of approximately 50 datasets that contain reviews of a specific product. Some companies provide products to Amazon Vine members, who are then required to publish a review.

I picked one of the datasets to perform the ETL process to extract the dataset, transform and load the data into a postgress data base by using an AWS RDS instance and pgAdmin.

Finally, I used Pandas to generate some information in order to determine if there is any bias toward favorable reviews from Vine members.


## Results

I picked a dataset that contains reviews about pet’s products as it is showed below

 ![image](https://user-images.githubusercontent.com/107591542/194208801-639f64f2-cbc6-40ff-bb06-b2d7e8d58ef9.png)


This dataset has 2,643,119 records
### How many Vine reviews and non-Vine reviews were there?
There are 10,215 Vine reviews and 2,633,399 non-Vine reviews. Only 0.3% of reviews was written by Vine reviewers so I can conclude that vine reviews don’t have a significant impact on results.

### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
After performing some filters indicated in the challenge instructions: retrievie all the rows where the total_votes count is equal to or greater than 20, all the rows where the number of helpful_votes divided by total_votes is equal to or greater than 50% and others We got these figures.

![image](https://user-images.githubusercontent.com/107591542/194209053-47180612-210b-49d9-9843-e15295ca40a8.png)

 
There are 170 vine reviews but only 65 of them are 5 stars

![image](https://user-images.githubusercontent.com/107591542/194209198-223fb9c9-6acc-4121-9c6c-00a8e1bd94bf.png)

 
There are 37840 non-vine reviews and 20612 of them are 5 stars

### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

•	Percentage 5star_vine reviews = 38.24% (65 / 170)

•	Percentage 5star_non-Vine reviews = 54.47% (20612 / 37840)

## Summary

Percentage 5star_vine reviews and Percentage 5star_non-Vine reviews are no comparable because they are really different ( more than 16 points). It looks that there is not any bias toward favorable reviews from Vine members.

Therefore, we could conclude that there isn’t a direct relation between the kind of reviewer (paid or unpaid) and the star rating. 
