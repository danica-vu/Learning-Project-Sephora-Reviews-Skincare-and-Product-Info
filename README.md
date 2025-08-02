# Learning-Project-Sephora-Reviews-Skincare-and-Product-Info

The entirety of this project is based on this data set that was collected by Nady Inky on Kaggle: https://www.kaggle.com/datasets/nadyinky/sephora-products-and-skincare-reviews/data

# Background
This is a learning project aimed at gaining some experience with MySQL and Power BI in order to create insights about customer reviews relating to skincare products sold at Sephora.
The end product of this project is a dashboard providing information on what is the most reviewed and recommended. 

With the data from the Python scrape, thanks to Nady Inky, there is data on all of Sephora's products and reviews on Sephora's skincare products as of March 2023. With Skincare becoming the new trend and focus of the beauty community, it is important to keep an eye on what people are talking about the most. 

# The Database
The original dataset was wonderful; however, some columns were not necessary, and some cleaning needed to get done. 
From the original dataset, I got rid of review_title and review_text because they contained characters that are not compatible with MySQL, despite being a regular CSV file. I changed the character set to UTC-8 in MySQL to try to accommodate, but to no avail.
I reformatted the submission time to the correct format to input into MySQL.
In the end, I created tables for the CSV files to sit in, and they were very much identical to the original, just without the review_title and review_text from the reviews table.

<img width="500" height="611" alt="Image" src="https://github.com/user-attachments/assets/63890452-dc12-40eb-a667-e82c136ed8fc" /> <img width="500" height="429" alt="Image" src="https://github.com/user-attachments/assets/22f278d9-c736-44f5-b870-6f6fedb8ab30" />

The final dataset had two tables: reviews and product_info. The product_info table had information on all of the products sold at Sephora as of March 2023, with 8,494 records. The reviews table held all of the reviews pertaining specifically to Skincare products or products with the Primary Category being Skincare from 8/28/2008 - 3/21/2023, with 1,094,411 records.

<img width="701" height="860" alt="Image" src="https://github.com/user-attachments/assets/3254f431-8662-4883-a392-727be4263b77" />

# The Dashboard
With all of my records uploaded to the tables. I focused on the number of recommendations and the number of reviews that were made on the skincare products. The number of reviews and recommendations would communicate brand and product popularity.

I wanted to work with Power BI in this project, but I knew that the 1 million records from the reviews table would decrease the efficiency of my laptop. I narrowed it down to a table containing brand name, product name, review quantity, recommendations quantity, and the subcategories of the skincare products (ex., sunscreen, bath and body), and whether the product was online and out of stock. 

The SQL to query the table is as follows:
<img width="1011" height="513" alt="Image" src="https://github.com/user-attachments/assets/b01fdead-fc21-4235-afaf-c54c6fd94ab4" />

Using the table, I was able to populate the dashboard with a main bar chart visual, a search function using an add-on by Microsoft, filters for the categories, and number metrics at the very top. The table below the bar chart serves as a way to see how popular a product is on the bar chart when you click on the product name and it also shows whether an item is in-stock and/or online.

A snapshot of my final dashboard:
<img width="1278" height="717" alt="Image" src="https://github.com/user-attachments/assets/b094759a-b8fa-4dd5-9e0a-26540a504c0a" />
