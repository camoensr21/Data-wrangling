# Data-wrangling
this repository is about collecting tweets from twitter

# INTRODUCTION TO THE PROJECT
This project is about wrangling, assessing and cleaning for analysis purpose.

## The goal: 
Wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. 

## What are the data and where they come from?
The data which will be used are about people's dogs rating. The dataset that will be wrangled (and analyzed and visualized) are the tweets
archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous 
comment about the dog. These ratings almost always have a denominator of 10. 
WeRateDogs has over 4 million followers and has received international media coverage.

## Where those data come from?
For this project we have three sources for the data:
1) Enhanced Twitter Archive, which comes on a csv file fomat:
The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything. 
One column the archive does contain though: each tweet's text, which are used to extract rating, dog name, and dog "stage" 
(i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced.
" Of the 5000+ tweets, the author has filtered for tweets with ratings only (there are 2356).
2) Additional Data via the Twitter API
Back to the basic-ness of Twitter archives: retweet count and favorite count are two of the notable column omissions. 
Fortunately, this additional data can be gathered by anyone from Twitter's API. Well, "anyone" who has access to data for the 3000 most 
recent tweets, at least. The WeRateDogs Twitter archive and specifically the tweet IDs within it, will allow gathering this data for 
all 5000+. We're going to query Twitter's API to gather this valuable data.
3) Image Predictions File
The author ran every image in the WeRateDogs Twitter archive through a neural network that can classify breeds of dogs*. 
The results: a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that 
corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images).

## GATHERING THE DATA¶
data are available from three differents sources, which will require programmatic gathering according to the format and the source of 
the data.
Three pieces of data will be gathered :
The WeRateDogs Twitter archive, which is a .csv format : twitter_archive_enhanced.csv
The tweet image predictions, i.e., what breed of dog (or other object, animal, etc.) is present in each tweet according to a neural 
network. This file (image_predictions.tsv) is hosted on a server.
Each tweet's retweet count and favorite ("like") count at minimum, and any interesting additional data you find interesting. 

## Assessing Data

for the assessment, we will verify quality issues and structural issues in the data from each table. For the quality issues, we will 
refer to the content of each variable or columns from each table, for the structural aspect we will analyse each columns headers and 
rows. The assessment will be done for each table separately:
- twiter_archive_enhance
- image_predictions
- add_data

For the quality assessment we will consider those four dimensions: completeness, for missing values validity: Do the values fit to the 
scheme of the variable? Accuracy: Do the values make sense? Consistency

