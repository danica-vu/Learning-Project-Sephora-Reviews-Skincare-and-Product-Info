# Learning-Project-Sephora-Reviews-Skincare-and-Product-Info

The entirety of this project is based on this data set that was collected by Nady Inky on Kaggle: https://www.kaggle.com/datasets/nadyinky/sephora-products-and-skincare-reviews/data

# Background
This is a learning project aimed at gaining some experience with MySQL and Power BI in order to create insights about customer reviews relating to skincare products sold at Sephora.
The end product of this project is a report providing insight into what is the most reviewed and recommended. 

With the data from the Python scrape, thanks to Nady Inky, there is data on all of Sephora's products and reviews on Sephora's skincare products as of March 2023. With Skincare becoming the new trend and focus of the beauty community, it is important to keep an eye on what people are talking about the most. 

# The Database
The original dataset was wonderful; however, some columns were not necessary, and some cleaning needed to get done. 
From the original dataset, I got rid of review_title and review_text because they contained characters that are not compatible with MySQL, despite being a regular CSV file. I changed the character set to UTC-8 in MySQL to try to accommodate, but to no avail.
I reformatted the submission time to the correct format to input into MySQL.
In the end, I created tables for the CSV files to sit in, and they were very much identical to the original, just without the review_title and review_text from the reviews table.
