# Tweets-Academic-Citation-Network_Graph_Visualization
Tweets/Academic Citation-Network_Graph_Visualization

### Overview
This analysis is proposed to leverage NetworkX and its embedded functionalities to parse through crawled public data from Tweeter and attempt to study network centrality based on users/hashtags (nodes) and their behavioral relationships (edges) such as retweets, mentions and co-occurrence. The raw dataset (https://archive.org/details/twitter-ira) was released by Tweeter on Oct 17th, 2018 following 205 Presidential Election with selected topics covering Politics, Propaganda, Social Media, and so on. The original dataset includes more than 10 million Tweets and more than 2 million images. For computational simplicity purpose, the dataset had been trimmed down to 50,000 instances with time horizon stretching from 2013 to 2018. Firstly, the dataset was cleaned and preprocessed through feature selection and engineering. Attributed related to sender nodes (userid, screen_name), relationship nodes (user_mentions, retweet_userid) and Tweet content (created_at, hashtags) are retained. The data was then aggregated by data into time series format with all iterated value compiling into a list per day. Figure 1 visualizes different attributes such as Tweets and Hashtags in a time series graph. Figure

![image](https://user-images.githubusercontent.com/43327902/185522367-abe14f14-b73c-452c-b673-2f0cd955397f.png)

Figure 1. Daily Attributes of Tweets

To dig into the relationship and mutual impact of different vertex in the network, three experiments that focus separately on co-occurrence of hashtags, mentions, and retweets have been conducted using network analysis techniques as well output visualization.

##### Co-occurrence of hashtags
Four dates were picked arbitrarily to sample the hashtags quoted in Tweets for specific date. Figure 2 shows the visualized output. Hashtags as nodes are loosely connected mostly. On 2015-03-18, the hashtag nodes in the middle with high degree are “quotes” ,”quote” and “tvshow” with 19, 19 and 12 degrees in total, with each connected with several neighbors including tv show names, actor/actress and so on.

![image](https://user-images.githubusercontent.com/43327902/185522457-d9780adf-396d-452e-8028-4d35ec0fde25.png)

![image](https://user-images.githubusercontent.com/43327902/185522471-72af6bc1-cd09-43af-a23e-614f685a43c3.png)

Figure 2 Graph of Co-occurrence of Hashtags

##### Mentions among Tweeple
From the network graph of mentions among Tweeple on 2014-07-26 as an example, there is one user, potentially an enterprise Tweet account such as CNN News, is in the middle has been mentioned by multiple Tweeple. Further investigation is needed to dive into the Tweet content and figure out what messages spread out in this way.

![image](https://user-images.githubusercontent.com/43327902/185522535-d0ef1c35-2fcd-49c2-9384-8aadd15d04bf.png)

Figure 3. Graph of Mentions of Tweeple

##### Retweets among Tweeple

Retweets graph shows a little bit more interesting that several nodes has edge that connected back to themselves which indicates that they may just retweet their own original Tweet with more comments or reply to someone.

![image](https://user-images.githubusercontent.com/43327902/185522624-a98ca015-4138-4c1f-89b3-5222c9bc6655.png)

Figure 4. Graph of Retweets

