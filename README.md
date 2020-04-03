# Watson-CI-JTNP-Project-Parks
A repository for code related to the Creative Inquiry (CI) at Clemson University with IBM Watson investigating social media sentiment relating to Joshua Tree National Park (JTNP).  


# File Descriptions
There isn't exactly a set order you need to run the notebooks in, and you definitely don't need to run all of them.  Each was created with a specific purpose in mind. 

**Twint_Batch_Tweet_Pull_and_Combine.ipynb**
This is the way we recommend gathering tweets about a subject. It is slow but thorough. 
Uses the Twint library to scrape all tweets based on a search term and put them into a CSV file.  It also has some code at the end to combine the CSV's together but it doesn't work perfectly.  Use [MergeCSV](https://www.filesmerge.com/merge-csv-files) for combining your CSV's in the end

**Clean_data.ipynb**
What we used to clean the tweets such as removing URLs, special characters, weird symbols, etc.  

**Twitter_Scraper.ipynb**
We initially used this to gather tweets but some groups have been running into consistency issues with it.  It uses the TwitterScraper library to scrape tweets 

**NLU_Batch_Processing_with_Multithreading.ipynb**
Uses the Watson Natural Language Understanding (NLU) to analyze the sentiment and emotion of all tweets.  It is multithreaded with 20-30 threads to speed it up.  Fair warning, this can get expensive if you need to analyze more than 30,000 tweets.  Works great though. 

**Visualize_NLU_Results.ipynb**
R-notebook (won't run in Google Colab as of March 2020) to create some figures from the NLU data

**Bag_of_Words_and_Random_Forest_Analysis.ipynb**
Our attempt at training a custom model to identify if tweets have a positive/negative/neutral sentiment and if they are pro-park or anti-park or neutral.  We labelled more than 500 tweets and then trained the models on combinations of the tweets and tested it.  The code works, but the models weren't very good.  
