# Web scrapper
The goal of this project is to recommend the best online store in terms of price for users after comparing the price across the stores for various FMCG products. 
 - The data about the products is obtained via Web scrapping. 
## OVERALL APPROACH: 

The four tasks that will be done as a part of this exercise will be as follows:
 
    A. Data Acquisition  
    B. Data Cleaning 
    C. Data Integration 
    D. Exploratory Data Analysis and Recommendation
# Data Acquisition

## Approach:

 1.  Identify set of categories and products that we want to scrap from various online e-commerce platforms.
     >There are around 30 categories and 150 items identified for web scrapping
 2.  Choose e-commerce platforms 
     >Following platforms have been chosen for scrapping
     - Big Basket
     - DMart
     - Grofers
 3.  Search the products on the browser and observe the URL/AJAX calls made as a part of fetching data from server
 4.  Identify various CSS classes for product attributes like Product name, MRP, Special Price
 5.  Write code to perform web scrapping for each of the platforms and store the results in a separate CSV file for later use
     > The results are stored in respective csv files as follows
     - BigBasket.csv
     - DMart.csv
     - Grofers.csv
# Data Cleaning

## Approach:

 For each of thep files generated in the previous section, perform following cleanup steps
 1. Separate weight and measure to separate columns from weight column
 2. Calculate the derived column discount based on MRP and Special Price
 3. Drop duplicate products that may have arrived due to wrong search results given by the site
 4. Re-arrange columns in proper order
 5. Save final set of products in respective csv files as follows
     - BigBasket.csv
     - DMart.csv
     - Grofers.csv
# Data Integration

## Approach:

 For each of the files generated in the previous section, combine them into a single file as follows
 1. Load following scrapped and already cleaned files into separate data frames 
     - BigBasket.csv
     - DMart.csv
     - Grofers.csv         
 2. Join all the 3 data frames into a single data frame
 3. Sort the products based on product type and name so that related products will be together irrespective of he shop
 
 4. Write the data frame into a final file
      - concat.csv
