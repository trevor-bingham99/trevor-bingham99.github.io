---
layout: post
title:  "Housing Quetions and Data Collection"
author: Trevor Bingham
description: This post will explain the question I want to look into, and how I went about gathering data to do so. 
image: "../assets/images/housing.png"
--- 

## Idea Formation

The housing market is something that feels like everybody talks about. The increasing prices, how unpredictable it can be, the lack of diversity, there are many different aspects to look into. One aspect that I wanted to explore more deeply was the pricing of houses, and what features of a house are the most impactful in terms of price. To do this, I started looking for housing data from Utah, and found [this](https://opendata.gis.utah.gov/datasets/utah::utah-housing-unit-inventory/about) site that had a great data set on houses in a few counties in Utah, with information on their size, type, location and price. Once I had located this data set, there are a few different ways you could go about downloading the data for use. In my code, found [here](https://github.com/trevor-bingham99/Semester-Project/blob/main/project.py), I show multiple ways to do so. 

They have a convient page that lets you download it in a format of your choice, such as CSV, KML, or a GeoJSON file. In my code, I show how to load in the csv file and work with it that way if that is what you prefer. I also show how you could use selenium to go to the table itself and scrap the data from the site and build your dataframe that way. The site also had a query feauture that would generate a URL that had a JSON text that included the data that met the conditions of you query, which I have an exmaple URL included as well, and show how you can load that into a dataframe as well. There are many ways you could go about getting this data, and it is up to you to decide which method works best for you. In my code, I iclude all these methods, but the main ones I used for my EDA were web scraping and the JSON URL, and then I combined the results of the two in to one data frame to have some from both methods, while checking for duplicates to make sure that doesn't impact anything. 

## About the Data

The data set we are loading in has multiple columns, that have a lot of intersting information is contained within. There is information the shape of the house, the location, the price, the square footage, the year built, the type of dwelling, the acreage of the property, and more. So with this, there is a lot of interesting things to look into, which you can see how I do in [this](https://trevor-bingham99.github.io/2023/12/13/EDA.html) blog post. Luckily, the data is already cleaned for the most part, if you do load it in from the JSON method, I added some code to clean the column headers and I have also dropped an added column from that to combine the two dataframes later in the code. 

One thing to note about how I have collected the data, for the data collected via selenium and the JSON URl, I only got a portion of the data to load, as to scrape it all with Selenium would take hours with how I was able to get it to work. Because of this, we do need to keep in mind that the data will most likely not be totally representative of the data as a whole, but can still be used to gain some basic insights into the data. I did try to sort it by the price in descending order to focus in on the houses on the higher price spectrum, so that is also important to keep in mind as we move forward.

## Ehtical Concerns

For this all data we collect and use, we want to make sure it is in line with ethical principles and practices. In this case, the site is a site dedicated to having publicly available data, and as of when I wrote this post and did this analysis, there were no restrictions in the robots.txt file for the site that would impact the data. Due to this, we can feel confident that our data is good to use, and does not go raise any ethical concerns. 

## Conclusion

This data set should be a great starting point for a exploratory data analysis on housing prices, and what features seem to have the biggest impact on it for the Utah housing market. To see the data itself, [here](https://raw.githubusercontent.com/trevor-bingham99/Semester-Project/main/Utah_Housing_Unit_Inventory.csv) you can find the csv that I downlaoded from the site with all the data, and [this](https://raw.githubusercontent.com/trevor-bingham99/Semester-Project/main/HousingData.csv) will show you the data I was able to scrape while using Selenium myselft, stopping the code after an hour so as to move forward.