# Learning-Project-Sephora-Reviews-Skincare-and-Product-Info

The entirety of this project is based on this dataset that was collected by Nady Inky on Kaggle: https://www.kaggle.com/datasets/nadyinky/sephora-products-and-skincare-reviews/data

# Background
This is a learning project aimed at gaining some experience with MySQL and Power BI in order to create insights about customer reviews relating to skincare products sold at Sephora.
The end product of this project is a dashboard providing information on what is the most reviewed and recommended. 

With the data from the Python scrape, thanks to Nady Inky, there is data on all of Sephora's products and reviews on Sephora's skincare products as of March 2023. With Skincare becoming the new trend and focus of the beauty community, it is important to keep an eye on what people are talking about the most. 

# The Database
The original dataset was wonderful; however, some columns were not necessary, and some cleaning needed to be done. 
From the original dataset, I got rid of review_title and review_text because they contained characters that are not compatible with MySQL, despite being a regular CSV file. I changed the character set to UTC-8 in MySQL to try to accommodate, but to no avail.
I reformatted the submission time to the correct format to input into MySQL.
In the end, I created tables for the CSV files to sit in, and they were very much identical to the original, just without the review_title and review_text columns from the reviews table.

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
<img width="1279" height="719" alt="Image" src="https://github.com/user-attachments/assets/e1fafd4d-901c-4b8b-b7cd-6c5fc63a6c7b" />

# Executive Summary
With a finished dashboard, products and brands that are the most reviewed and most recommended can be determined. It is observed that the most reviewed brand is Clinique. Not only are they the most reviewed brand, but they also have the most reviewed Cleanser and Eye Care products. The product that single-handedly has the most reviews is the Lip Sleeping Mask Intense Hydration with Vitamin C by LANEIGE, which makes sense because during the time of the web scrape, this product was extremely popular. The results are achieved with the drill functions on the main bar chart. The lip mask also dominates the Lip Balms & Treatments product category. By using the menu on the left side, Skincare product categories can be filtered on a secondary and tertiary level. For Masks, Origin's Clear Improvement Charcoal Mask to Clear Pores is shown to be the most popular. 

For moisturizers, while Tatcha holds the most reviews overall, the product with the most reviews is the 100 percent Pure Argan Oil from Josie Maran. This seems to be also the case for Tatcha in the Mini Size category, where the brand has a lot of reviews, but the most reviewed product does not belong to the brand. This could mean that Tatcha is a magnetic brand with a strong identity, creating a uniform popularity with its products. This would make sense. With Tatcha being on the pricier side at Sephora and so many people buying their mini sizes, which are cheaper than the original sizes, it could mean that people like the brand and the fantasy of being luxurious attached to it. This also implies that Tatcha has been heavily marketing their products to a larger audience, selling this idea of luxury.

<img width="1279" height="717" alt="Moisturizers brand" src="https://github.com/user-attachments/assets/ab0757eb-0305-40dd-b366-90614bbcdc2f" /> 
<img width="1278" height="720" alt="Moisturizers Products" src="https://github.com/user-attachments/assets/c7716d4b-ac9b-4e5e-a12f-33668a52d7e3" />


For Self Tanners, Isles of Paradise, and their product Self Tanning Bronzing Face Drops take the lead. For Sunscreen, Supergoop! and their product Unseen Sunscreen SPF 40 PA +++ are the most reviewed. With the knowledge that an 'Unseen Sunscreen' is the most popular in the sunscreen category, Sephora should look into Korean sunscreens that specialize in this feature. They've already incorporated Inisfree into their stores, and their sunscreen is in 5th place for the most popular Sunscreen product. This is a newer addition to the store and is very close to the 4th place product, Clear Sunscreen Stick SPF 50+ by Shiseido. Shiseido has been a part of Sephora much longer than Inisfree, and with Inisfree having a rise in popularity in America, it should surpass Shiseido and go neck to neck with Supergoop! soon. Also worth mentioning, Inisfree sunscreen has all of the properties consumers are looking for in a sunscreen; this is something useful to know in predicting its popularity in the future. 


<img width="1278" height="719" alt="Sunscreen" src="https://github.com/user-attachments/assets/ffac9507-be76-4f07-91d8-fed77bec3883" />

When looking at treatments, what consumers have the most problem with reflects on what they will buy. In this category, treatments mean a lot of things (ex., serums, toners, peeling solutions, etc.), so utulizing the Tertiary Category feature would be the move to figuring out each subcategory. However, overall, the most popular treatment product aims to be used daily. Restocking this product and products aimed at being used in a daily routine would be ideal. Speaking of treatments, for the Value & Gift Sets category, people tend to talk about the self-care type of kits. Finally, in the Wellness category, people tend to talk about and recommend products that tackle their skin problems over their diet and mental health. This is something to keep an eye on because this category is on the more hidden or niche side of Sephora, and it could possibly show what people prioritize and care about. 

# Takeaways
I learned so much about the nuances of MySQL and Power BI. It could be easy to execute the commands and create a dashboard that works. However, I found that within these actions, I have to think about efficiency and relevance while having to do a handful of troubleshooting tasks. Troubleshooting is not my specialty, and if I learned one thing, it's that I should consider putting that into my toolbelt. 

Right now, I'm still learning DAX, and I originally wanted to use this skill in this project. However, the way I wanted to use it was to create a column in my table and calculate percentage values of positive and negative feedback as a number in the top row of the dashboard. This would've required me to input the entirety of the reviews table into Power BI, which would've slowed down my laptop. In my next project, I will look forward to incorporating DAX so I can gain experience with it.

This was such a great opportunity to work on my analytics skills, and this project opened my eyes to the possibilities of what I can contribute to by providing insights through data visualizations.


This Sephora Products and Skincare Reviews dataset by Nady Inky had a [Attribution 4.0 International (CC by 4.0)](https://creativecommons.org/licenses/by/4.0/) license on it.
