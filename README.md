# Amazon_Vine_Analysis

![248754-2119x1414-chianti-and-bruschetta](https://user-images.githubusercontent.com/108313440/197053415-42c1b0ad-ddf7-4170-a82a-6e6d62c2af3b.jpg)

## overview of the Project
This project analyzes Amazon reviews written by members of Amazon Vine's paid program. Vine is a service that lets publishers and manufacturers receive reviews of their products and determines whether there are any biases among Vine and non-Vine reviews.
Vine members may receive free products in exchange for reviews, which Amazon will collect from the companies. Our goal is to assess whether there is any bias towards favorable reviews by Vine members vs. non-members based on the number of 5 star ratings to total ratings. In order to complete our analysis, we were required to choose 50 datasets to extract, transform, and load into a dataframe.

## Resources
* DataBase was chosen from "Wireless" categorey and can be dwonloded from [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Wireless_v1_00.tsv.gz)
* Google Colab (to run PySpark)
* Jupyter Notebook
* AWS S3 and RDS
* PostgreSQL


## Summary of the Results
First, the dataset was extracted from AWS S3 using PySpark, transformed, and finally reloaded into postgres AWS.
### Deliverable 1: Perform ETL on Amazon Product Reviews 
In the fisrt deliverable, we created four dataframe named customers_df, products_df, review_id_df, and vine_df. Then, the data frames were loaded into pgAdmin. To this end, I initially made the connection to my AWS RDS instance. After that, I loaded the DataFrames that corresponded to tables in pgAdmin. To make sure that the table had been populated, I ran a query In pgAdmin.

<img width="1108" alt="Screen Shot 2022-10-20 at 6 32 32 PM" src="https://user-images.githubusercontent.com/108313440/197071884-2b63834a-b4d7-4627-8a0b-e09350936aa8.png">

<img width="936" alt="Screen Shot 2022-10-20 at 6 32 40 PM" src="https://user-images.githubusercontent.com/108313440/197071905-a08ef48a-0d76-4558-a6ef-732adf773ce5.png">


<img width="1295" alt="Screen Shot 2022-10-20 at 6 32 50 PM" src="https://user-images.githubusercontent.com/108313440/197071922-753019bd-30ad-4e69-ab0a-e5bf074ce39e.png">

<img width="975" alt="Screen Shot 2022-10-20 at 6 32 59 PM" src="https://user-images.githubusercontent.com/108313440/197071950-65c557ff-1fb8-4bfa-868f-43ede03a8cc3.png">


<img width="996" alt="Screen Shot 2022-10-20 at 9 20 45 PM" src="https://user-images.githubusercontent.com/108313440/197089573-ca3a942e-4c7a-4f27-b67d-0583c6a8d321.png">

<img width="1013" alt="Screen Shot 2022-10-20 at 9 22 01 PM" src="https://user-images.githubusercontent.com/108313440/197089577-5960e849-b985-4c83-8d61-d3f72ec65973.png">

<img width="1004" alt="Screen Shot 2022-10-20 at 9 22 48 PM" src="https://user-images.githubusercontent.com/108313440/197089578-14f5f739-d657-4ba1-a978-6cf90b268aad.png">

<img width="1003" alt="Screen Shot 2022-10-20 at 9 23 25 PM" src="https://user-images.githubusercontent.com/108313440/197089579-86020621-63a8-4aa7-865a-8f253d38389c.png">

### Deliverable 2: Determine Bias of Vine Reviews
In this step, I determined if there was any bias towards reviews that were written as part of the Vine program using PySpark. For this analysis, I determined if having a "paid Vine review" makes a difference in the percentage of 5-star reviews.	To this end, the first step was creating a new DataFrame by filtering the data in vine_df to retrieve all the rows where the total_votes count is equal to or greater than 20 to pick reviews that are more likely to be helpful and to avoid having division by zero errors later on. Then, we filtered  the DataFrame created in the previous step and created a new DataFrame to retrieve all the rows where percentage of helpful_votes was equal to or greater than 50%.  This was followed by filtering  the DataFrame created in Step 2, and create a new DataFrame that retrieved all the rows where a review was written as part of the Vine program (paid). Finally, we repeat Step 3, but this time retrieved all the rows where the review was not part of the Vine program (unpaid)

<img width="1299" alt="Screen Shot 2022-10-20 at 6 33 37 PM" src="https://user-images.githubusercontent.com/108313440/197071973-a7d066cc-ce41-4172-bc23-71679886cb81.png">

<img width="1337" alt="Screen Shot 2022-10-20 at 6 34 11 PM" src="https://user-images.githubusercontent.com/108313440/197071997-ea7aede6-3e09-4fe9-81c8-4c7737904326.png">

<img width="888" alt="Screen Shot 2022-10-20 at 6 34 21 PM" src="https://user-images.githubusercontent.com/108313440/197072020-778a3eea-0faa-4ff7-a9ca-5e0b2a0a02be.png">

<img width="873" alt="Screen Shot 2022-10-20 at 6 34 33 PM" src="https://user-images.githubusercontent.com/108313440/197072062-42109b9f-0c37-41a4-a228-4ba80e12d29e.png">

## Summary

<img width="612" alt="Screen Shot 2022-10-20 at 6 35 20 PM" src="https://user-images.githubusercontent.com/108313440/197072076-c1c74c7e-1f1d-4685-ae3a-6992df69a26d.png">








