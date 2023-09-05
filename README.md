# Case Study: Youtube Statistics

This is my first data analytics case study, completed as the capstone project for the Google Data Analytics Professional Certificate. For this study, I will be analyzing global youtube statistics to gain insight on how a hypothetical media group can grow their YouTube channel.

## Ask

The business task I have been assigned is helping "QWERTY Media" grow their YouTube channels with insights gleaned from YouTube's top channels. 

The stakeholders are the following:
- Cofounders Tom and James Qwerty, two brothers who started their youtube channel and the media group after gaining popularity on Vine.
- Their investors.
- QWERTY Media's management, marketing, and editing teams.

There are several questions the company wants to answer through this analysis:
- How often should their channels upload? Do more uploads per week correlate to higher subscriber gains?
- Should QWERTY Media create side channels in other languages? Which countries are the most popular channels located in?
- In regards to content creation, which channel types are currently trending? Which are the most profitable?

QWERTY Media hopes that the insight gained in this study will help guide their content creation strategy to optimize subscriber gains.

## Prepare

The data set I will be using for this study is [Global YouTube Statistics 2023](https://www.kaggle.com/datasets/nelgiriyewithana/global-youtube-statistics-2023), posted on Kaggle by Nidula Elgiriyewithana. This data set contains statistics on the top 995 YouTube channels by subscriber count.

The following information is included: 
- YouTube Channel names, category and channel type, total subscribers, total video views, number of uploads, and date channel was created
- The country the channel is assigned to, that country's latitude and longitude, and statistics on the country's population, unemployment rate, and gross tertiary education enrollment
- The number of subscribers and videos views gained by a channel in the past month
- Rankings based on location and channel type
- Monthly and yearly earnings for each channel


  
## Process

After crossreferencing the data set with the information from Youtubers.Me, the following cleaning was done in Google Sheets:
- Broken character names were fixed
- Errors found in dates, upload counts, countries, and channel types were fixed
- Removed data from deleted or unverifiable channels

The rest of the cleaning was done in R Studio. The full process phase can be found in the (R Markdown File).

The following processing was done in R Studio:
- Column names were cleaned for consistency
- Dropping channels that had 0 total video views
- Dates were concatenated into a single column
- Dropped columns unecessary for analysis
- Changing missing qualitative data to "Unassigned" for filtering
- Changing NaN quantitative data into standard nulls

## Analyze

The full analysis phase can be found in the (R Markdown File).

In the analysis phase, I returned to the questions from the ask phase.
In order to find how the frequency of uploads affected subscriber gains, I found the average weekly upload counts and the average weekly subscriber gains for each channel.
(image of table)
(image of plot)
The data shows there is barely a correlation between the amount of weekly uploads and subscribers gained. Plenty of channels uploading frequently are getting less subscribers than ones that do.

Next was finding the distribution of subscribers gained in the last month.
(image of plot)
The channel type with the highest distribution is Animals, with Comedy and People the next highest. Notably, Entertainment has several extreme outliers.  

I then found the average yearly earnings for each channel.
(image of table)
I made another boxplot showing the distribution of average yearly earnings.
(image of plot)
Looking at our new box plot, Animals is also the channel type with the highest distribution of average yearly earnings, with News and Comedy behind it.

Finally, the last step was finding the percentage of the top channels each country made up.
(image of table)
The top five countries are the United States, India, Brazil, the United Kingdom, and Mexico.

## Share

(Link to view completed Tableau Dashboard.)

## Act

Based on the analysis, these are the key takeaways for QWERTY MEDIA:

- The company should focus on fewer, higher quality videos each week rather than constant uploads.
- To increase engagement and yearly earnings, the company should consider Animals, News, Comedy, and People in their content direction.
- As QWERTY Media is already based in the United States and the primary language in the United Kingdom is English, a secondary channel for English speakers is unnecessary. QWERTY Media should instead consider making secondary channels in Hindi, Portuguese, and Spanish to potentially reach new audiences in India, Brazil, and Mexico.

The next steps I would suggest for QWERTY MEDIA:
- Find trending channels in their categories of focus (Animals, News, Comedy, and People) in their countries of focus (India, Brazil, and Mexico) to see what makes these channels sucessful.
- Reach out to these trending channels to find partnerships and collaborations.

