# Wrangle and Analyze Data

Introduction
This Wrangle and Analyze Data Project is part of Udacity's Nanodegree Data Analyst program. This project involved wrangling (and analyzing and visualizing) data from the Twitter user @ WeRateDogs, collected from different sources connected with the tweets. WeRateDogs is a Twitter account that rates photos of people's dogs in a humorous way. These ratings almost always have a denominator of 10.

Objectives
The aim of this project is to “wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations”.

To achieve the aim of this project, there are some objectives that need to be fulfilled. Data Gathering: This involves gathering the data to be used. We are going to gather data from a variety of sources. Accessing: assessing the data to gain better understanding of the data. Cleaning: this involves cleaning the data. The other steps involve Storing, analyzing, visualizing, and reporting on the wrangled data.

Gathering Data
There were three different data used for this project: twitter archive file, twitter API and an image tweet prediction file.

1. The twitter_archive_enchanced.csv was provided and downloaded manually from the Udacity classroom. The file contains specific variables for each tweet including tweet Id, name,  timestamp, text, number, and denominator ranking  etc.

2. The tweet image predictions file was programmatically downloaded from Udacity 's servers using the Requests Python library. This file had the breed of dog, which was predicted based on the picture, using machine learning techniques.

3. Twitter API and Python's Tweepy library was used to  gather each tweet's retweet count and favorite ("like") count at minimum.



Accessing Data
After gathering all three pieces of data, the data was assessed visually and programmatically (pandas’ library) for quality and tidiness issues. At least eight (8) quality issues and two (2) tidiness issues were detected and documented.

Quality Issues:

1. Timestamp is not of datetime format.

2. Wrong Datatype: Column’s tweet_id and img_num should be in string.

3. Invalid names: Columns such as Name contain some invalid names.

4. There are 59 null entries in the expanded_urls column.

5. rating_denominator column should only have the denominator value - 10

6. rating_numerator that have values lower than 10 that should be removed.

7. There are capitalized and lower-cased names in the p1, p2, and p3 columns

8. Extracting ratings from the text of the tweet and be used to fill in the rating_numerator column by finding patterns.

Tidiness Issues:

1. Dropping columns not needed. (in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id, and retweeted_status_timestamp) The columns have too many null values in them.

2. Merging the clean versions of the data files together; twitter, image, and json dataframes.

3. Creating one column for the various dog types (doggo, floofer, pupper, puppo).
Cleaning Data

All  of the issues documented above while assessing the data files were cleaned. I cleaned the data through the following means:
Define, Code and Test:

• Timestamp format is incorrect. The timestamp data type was changed  from object to datetime

• Data type of tweet_id should be string, not object.  I changed the tweet_id  of all the data frame to string.

• Dog names "None", "a", "the" and "an"  was replaced.

• The expanded_urls column that has null values was dropped. There are 59 total that we observed from the assessments.

• The rating_denominator column was set to have only denominator 10.

• Numbers fewer than ten were excluded from the numerator column.

• Replaced all dog names in these columns with a lower-case letter.

• Extracted numerator ratings from the tweet text and to fill in the missing values in rating_numerator column by finding the pattern

• Dropped columns not needed

• Created one column for all the dog types.

• Merged the clean versions of the dataframes

- Conclusion: The merged cleaned data frame was stored (dog_twitterpage), analyzed, and visualized. The project taught how that real-world data are rarely found in a single source and must be combined from multiple sources before any sort of analysis can be performed. It also aided my understanding of how tidiness and quality concerns can arise in data, as well as how to deal with them.
 
