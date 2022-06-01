# Airbnb-Successful-Host-Analysis-in-LA
*Evaluation system and recommendations for new hosts penetrating hospitality market.
- Processed data of 120,000 records of listings and built a model to reveal the feature set affecting superhost recognition, helping increase booking rate and improve customer experience.
- Implemented explanatory analysis and machine learning model to detect the reason for revocation of the Super-host title (accuracy 73%)
*Applied text mining and sentiment analysis on more than 1 million reviews to discover customers’ considerations when staying in an Airbnb, resulting in suggestions for increasing rating scores.

1. AIRBNB SUPERHOST OVERVIEW

- Every 3 months, Airbnb evaluate host performance and check whether a host hit all the requirements within the past year to become Superhost. If a host satisfies the performance standards and other qualifications for the most recent 12 months from the review date, then the host is automatically eligible to become a Superhost for the qualification period. (For example, if the review date is on July 1, 2014, then a host’s performance from the most recent previous 12 months from July 1, 2014 is measured.)
Superhost status is automatically revoked at the next review date if the host did not meet the performance standards during the most recent 12 months. Hosts who have had their Superhost status revoked may regain their Superhost status during a future qualification period if they meet the qualifications for the most recent previous 12 months on that review date.
When qualifying to become a Superhost, a badge indicating host status as a Superhost will automatically be added to host’s Airbnb profile and listing pages for as long as host continue to qualify. 
**Criteria for being Super host:
- Overall rating > 4.8
- Completed 100 nights over at least 3 completed stays
- <1% cancellation rate
- 90% response rate
**Superhost Benefits:
-	Welcome more guests - Earn extra money
Superhosts often benefit from a significant increase in earnings. More visibility and trust from guests can lead to more bookings, which means more money for hosts. 
-	Get special recognition 
Guests trust that Superhosts are the best of the best and can filter their search results to discover only listings with Superhost status. Airbnb promotional emails and Superhost badges help them stand out even more.
-	Gain access to exclusive rewards
Superhosts earn a $100 Airbnb travel coupon every year that they keep their status. And when they refer a new Host to sign up, Superhosts get an extra 20% on top of the usual referral bonus.

2. BUSINESS OBJECTIVES

It is helpful for Airbnb to determine potential hosts among new hosts and then highlight them, supporting valuable hosts and increasing the customers’ experience. Therefore, this project will analyze SUPERHOSTS, with many previous bookings and high customer score rates. We try to find out the pattern of SUPERHOSTS; we provide suggestions for new hosts to improve their services. There are three business objectives in this project:
•	Which features of hosts and their listings help them to become SUPERHOSTS?
•	Which features will threaten the super host status?
•	How do guests’ reviews help the HOSTS improve services?

3. DATA CLEANING

The Listing data is all Airbnb listings in Los Angeles and collected by scraping from the Airbnb website in June, September, and December of 2021. Because these data are scraped, numeric variables, such as “Price,” “Response Rate,” and “Acceptance Rate,” are presented as characters. First, we change numeric variables in the wrong data types into correct ones.
Next, we deal with missing data. We replace the missing value in the “numbers of beds” variable with the average of this variable grouped by the room type. Similar to the “Acceptance Rate,” we replace missing values in this variable with the average acceptance rate.
We have “longitude” and “latitude” variables; we want to transfer these variables into zip codes to get more of the demographic in the listing’s area. We use Google API to change longitude and latitude into Zip codes. Then based on Zip codes, we added two additional about the area’s population density and the percentage of population under poverty.
We have a character variable called “amenities,” including a list of amenities that the Airbnb listing has; the form of this variable is not helpful in our future models, so we use R functions to create new numeric variable counting how many amenities the listing has. In addition, we make new dummy variables that present whether amenities, such as TV, parking space, kitchen, coffee machines, BBQ, balcony, or air conditioner…, are offered or not.


4.	VISUALIZATION

There are 30% superhosts (5521) in total of 18398 hosts of Airbnb in Los Angeles. There are many factors that affect whether a host is recognized as superhost or not. An interesting fact is that the average price of each room type (Entire home/apt, Hotel room, Private room, Share room) of superhost is lower than that of host, but the host’s listings have a wider range of prices than superhost’s listings. The response rate and acceptance rate of superhost are pretty higher than that of host, response time of superhost is also faster. Superhost’s listings have more amenities than the host’s and average review scores are also much higher.  




