---
layout: post
title:  "Housing Quetions and Data Collection"
author: Trevor Bingham
description: This post will explain the question I want to look into, and how I went about gathering data to do so. 
image: "../assets/images/housing.png"
--- 

## Idea Formation

The housing market is something that feels like everybody talks about. The increasing prices, how unpredictable it can be, the lack of diversity, there are many different aspects to look into. One aspect that I wanted to explore more deeply was the pricing of houses, and what features of a house are the most impactful in terms of price. To do this, I started looking for housing data from Utah, and found [this](https://opendata.gis.utah.gov/datasets/utah::utah-housing-unit-inventory/about) site that had a great data set on houses in a few counties in Utah, with information on their size, type, location and price. Once I had located this data set, there are a few different ways you could go about downloading the data for use. In my code, found [here](https://github.com/trevor-bingham99/Semester-Project/blob/main/project.py), I show multiple ways to do so. 

They have a convient page that lets you download it in a format of your choice, such as CSV, KML, or a GeoJSON file. In my code, I show how to load in the csv file and work with it that way if that is what you prefer. I also show how you could use selenium to go to the table itself and scrap the data from the site and build your dataframe that way. The site also had a query feauture that would generate a URL that had a JSON text that included the data that met the conditions of you query, which I have an exmaple URL included as well, and show how you can load that into a dataframe as well. There are many ways you could go about getting this data, and it is up to you to decide which method works best for you.

## About the Data

The data set we are loading in has multiple columns, that have a lot fo intersting 