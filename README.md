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
First, the dataset was extracted from AWS S3 using PySpark, transformed, and reloaded into AWS.

<img width="1108" alt="Screen Shot 2022-10-20 at 6 32 32 PM" src="https://user-images.githubusercontent.com/108313440/197071884-2b63834a-b4d7-4627-8a0b-e09350936aa8.png">

<img width="936" alt="Screen Shot 2022-10-20 at 6 32 40 PM" src="https://user-images.githubusercontent.com/108313440/197071905-a08ef48a-0d76-4558-a6ef-732adf773ce5.png">


<img width="1295" alt="Screen Shot 2022-10-20 at 6 32 50 PM" src="https://user-images.githubusercontent.com/108313440/197071922-753019bd-30ad-4e69-ab0a-e5bf074ce39e.png">

<img width="975" alt="Screen Shot 2022-10-20 at 6 32 59 PM" src="https://user-images.githubusercontent.com/108313440/197071950-65c557ff-1fb8-4bfa-868f-43ede03a8cc3.png">


<img width="1299" alt="Screen Shot 2022-10-20 at 6 33 37 PM" src="https://user-images.githubusercontent.com/108313440/197071973-a7d066cc-ce41-4172-bc23-71679886cb81.png">

<img width="1337" alt="Screen Shot 2022-10-20 at 6 34 11 PM" src="https://user-images.githubusercontent.com/108313440/197071997-ea7aede6-3e09-4fe9-81c8-4c7737904326.png">

<img width="888" alt="Screen Shot 2022-10-20 at 6 34 21 PM" src="https://user-images.githubusercontent.com/108313440/197072020-778a3eea-0faa-4ff7-a9ca-5e0b2a0a02be.png">



<img width="873" alt="Screen Shot 2022-10-20 at 6 34 33 PM" src="https://user-images.githubusercontent.com/108313440/197072062-42109b9f-0c37-41a4-a228-4ba80e12d29e.png">

<img width="612" alt="Screen Shot 2022-10-20 at 6 35 20 PM" src="https://user-images.githubusercontent.com/108313440/197072076-c1c74c7e-1f1d-4685-ae3a-6992df69a26d.png">








