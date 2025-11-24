# Personal Library Book Analysis

## Introduction
For this personal dataset project I decided to explore the books in my library. The initial data came from scanning all of the books and scraping some data from their ISBN codes through the Android Book Catalogue app. The initial DeFordBooks.csv was exported from the app directly. 

## Data Processing

In order to carry out the analysis below, I removed some columns that were mostly empty or didn't have interesting information and condensed some of the columns that had too many classes. I also added a couple of binary columns (kids and math) to make some of the analysis easier. The transformed data is uploaded here, along with the processing script. 

## Exploratory Analysis

The main numerical column on the data is the number of pages, although I also added a column that counts the length of the description of the book. The plot below shows the histogram of these description lengths: 

https://github.com/drdeford/MATH144_PDP/blob/main/desc_length.png

![Histogram of description lengths of books in my library](https://github.com/drdeford/MATH144_PDP/blob/main/desc_length.png)


## Logistic Regression

It looked like the number of pages was quite different between the kid books and math books, so I fit a logistic regression model to see if I could predict which type a book was based on the number of pages. The following figure shows the predicted probabilities for the books in the dataset, and the model correctly classified over 97% of the books. 
