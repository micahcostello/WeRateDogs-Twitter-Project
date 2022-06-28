# WeRateDogs-Twitter-Project

In this project, I went through all the steps of the data analysis process. My end goal was to glean insights from data from the Twitter page WeRateDogs.

I began by gathering the necessary data from three sources: the Twitter archive, provided as a .csv file; a file full of image predictions based on the tweets, provided as a .tsv file in a url; and data from the Twitter API. The most challenging of the three was the API data without a doubt. I had to query all of the tweets by looping through the tweet ids from the Twitter archive file. I pulled information like like count and retweet count. I converted each query to a json string and loaded it into a file “tweet_json.txt”. Then, in a second loop, I converted each line of the file to a dictionary to append to an empty dataframe.

Once the data was gathered, I assessed it for cleanliness and tidiness issues. I employed methods of visual assessment (Pandas . head(), .tail() ) as well as programmatic assessment ( Pandas .info(), .describe() ). Some issues, such as multiple columns for the same variable “dog stage”, were immediately clear. Others required further investigation, such as the existence of tweets without images.

The major issues revealed by assessment were ones of inaccurate data. For example, some of the tweets were retweets- I only wanted original tweets. Some of the ratings were inaccurately extracted from the Twitter archive, and some original tweets were either without images or were images that weren’t about dogs. Other issues were less serious, such as incorrect dog names or unwieldy values in the source column.

No matter the gravity of the issues detected during assessment, I cleaned them all using the define-code-test method. All of the inaccurate data was removed or corrected, and the datasets were re-organized to correct tidiness issues, such as the multiple dog stage columns. Then, I corrected the overarching tidiness issue: all the data being in three separate dataframes. I merged the data from the three sources into one master dataframe.

Once all the data was made tidy, clean and accessible, I used the opportunity to augment the data. I created a month column which proved essential for analysis.

Finally, I stored the master dataframe to a .csv file and began analysis. I tried to determine how the WeRateDogs twitter page changed over time. Without the wrangling I completed, the analysis would have either been impossible or led to incorrect conclusions.
