# FakeCOVID
FakeCOVID is collected to address the issue of fake news/claims about COVID-19 during the pandemic. 
## Overview
FakeCOVID is a comprehensive dataset which contains:
* **News content** is stored in `./source/`
* **Labels & Explanations (News Reviews)**: are stored in `./reviews/`
* **Twitter Engagements**: The engagements on twiiter include tweets, replies, quotes and retweets. Due to the privacy policy of Twitter, only the tweet IDs and User IDs are provided in  `./twiiter.json`.
* **Reddit Engagements**: The engagements on twitter include submissions and quotes. They are stored in `./reddit/`

## Statistics of the Dataset
|            | Total  | False  | Mixture | True  |
|------------|--------|--------|---------|-------|
| News       | 102    | 64     | 23      | 15    |
| Submission | 1573   | 862    | 568     | 143   |
| Comment    | 65781  | 51400  | 12660   | 1721  |
| Tweet      | 199130 | 123295 | 39083   | 36752 |
| Reply      | 200734 | 112774 | 58874   | 29016 |
| Retweet    | 265937 | 161368 | 35132   | 39337 |
| Quote      | 67838  | 36768  | 25217   | 5853  |
| User       | 555802 | 343500 | 156313  | 95507 |

## Data Format
* source
  * <news_id>.json: contain the features of the news such as **Title**, **Text**, **Tags**, **Key Words**, **Authors**, and **Date**.
* reviews
  * <news_id>.json: the features include: **Rating of the News**, **True Part**, **False Part**, **Review Title**, **Explanations**, **Source link**, **Images**, **Date**, and **Support Links**.
* reddit
  * <news_id>
    * Submissions
      * <submission_id>.json: includes **ID**, **Created Time**, **Author Profiles**, **Title**, **Selftext**, **Upvote Ratio**, **URL**
    * Comment
      * <comment_id>.jons: includes **ID**, **Created Time**, **Author Profiles**, **Score**, **Submission ID**, **Permalink**.
* twitter.json: a dictionary contains the **news_id**, **tweet_id** ,**reply_id**, **quote_id**, and **retweet user id** 
