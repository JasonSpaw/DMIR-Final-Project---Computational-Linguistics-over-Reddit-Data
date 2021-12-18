Thise was the final project for DMIR course involving uploading to database, creating triggers, sentimental analysis, topic modeling, phrasing and database queries.

# DMIR Final Project - Computational Linguistics over Reddit Data

- For this project, pull Reddit subposts from 5 programming related subreddits into a PostGres database, created triggers to implement vector models to aid in search queries, and analyzed sentiment across subreddits from different fields/job titles related to computer programming, such as datascience, machinelearning, dataanalytics, gamedev (wanted to compare field that might attract more artistic applications), and robitics (to compare a field that might attract those that like to tinker with mechanical engineering side while also applying programming/machine learning). The goal is simple, to observe sentimental trends and see if the users utilizing the subreddits, assuming those posting on the subreddits are working or studying those fields, enjoy their field more than others enjoy theirs as a whole, or perhaps there is very little to no deviation between the fields in which case it is all relative to the individuals. I also looked at topic and phrase modeling to support my claims.

Sentiment Analysis of Programming Subreddits:

![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/DMIR%20Final%20Comp%20Scores.png)

- DataScience appears to have the highest compound score on average, meaning it carries the highest amount of positive sentiment, followed by gamedev and MachineLearning. Not as much enthusiasm in robotics.  As a whole, none of the subreddits experienced any real negativity, with most submissions primarily carrying high neutral sentiment scores meaning that these subreddits are likely more informative and a place for users to help one another with programming related issues and questions.

Topic Modeling:

- I used Non-negative Matrix Factorization to obtain and observe the top ten topic models for each subreddit to visualize what is primarily being discussed in the subreddits.

For datascience:

- Topic  0 data science product scientists years know analyst use like manager
- Topic  1 salary senior month level year median responsibilities years offer couple
- Topic  2 file files access sample number approach second memory _getitem id
- Topic  3 explanatory time models variables customer churn looking user prediction frequency
- Topic  4 different data file way column image proper folder drive text
- Topic  5 like job working work feel role data months break people
- Topic  6 recall user precision data model specific low high set instances
- Topic  7 excel data dashboard help steps qlik like need sql guys
- Topic  8 research papers learning ml week trying like reading think paper
- Topic  9 ve project just work python new use lot methods cool

For MachineLearning:

- Topic  0 space boundaries samples decision label training layer neural output input
- Topic  1 ve learning job position machine engineer experience role ml small
- Topic  2 data feature mlp image tabular learning think extractor trained pre
- Topic  3 spin model vector attention statistical partition mechanics transformer differentiable transformers
- Topic  4 pytorch docker template use source version universal cudnn increase using
- Topic  5 point camera image novel rendering differentiable cloud rasterization neural network
- Topic  6 like voice good sound person data specific ones know make
- Topic  7 data method research nlp readiness academic researchers stakeholders academia projects
- Topic  8 transformer audio representation task speech representations quantized latent model exactly
- Topic  9 3d data vision models computer learning used like world understanding

For dataanalytics:

- Topic  0 omnisci analytics data using aws platform solutions nvidia scaling laptop
- Topic  1 number calls customer customers employees service feature 10 total just
- Topic  2 data analytics masters job help learn sql courses want business
- Topic  3 omnisci data use cns network sites make new ll performance
- Topic  4 event sales data prediction curve fitting weeks events forecast looking
- Topic  5 ibcs company report data reports deliver business think look want
- Topic  6 data science career 000 job analytics openings field technology 2020
- Topic  7 x200b did test using spss expert modeler values acf arima
- Topic  8 health program care course currently appreciate start working year analyst
- Topic  9 analytics ve data thanks problem platforms post responses field research

For gamedev:

- Topic  0 game people lot time nbsp make don job good idea
- Topic  1 game trailer views day know posted people ll twitter things
- Topic  2 game x200b people just blocks games make minecraft like really
- Topic  3 int frame thread lua coroutine scripting java print game using
- Topic  4 server player game new client doing position players connected packets
- Topic  5 items array item tab going displays use window inventory way
- Topic  6 x200b levels short decided make game level stuff finally im
- Topic  7 like game want ve don make use just know art
- Topic  8 object dof matrix need affine regular relative ve seesaw launch
- Topic  9 service cloud provider team shared plan game goes title happens

For robotics:

- Topic  0 robot mm need ready software used controller know fully 250
- Topic  1 engineering program department home computer courses ae ms robotics working
- Topic  2 x200b robotic don place engineer help know year months core
- Topic  3 like start parts pla really buy best white remember black
- Topic  4 problem robot cylinder simulation conveyor robotics help looking kind want
- Topic  5 team foxglove share layouts studio feedback app organization teammates robotics
- Topic  6 robots stacking simple job various deepmind researchers new robotics need
- Topic  7 servo arm little base robot motor gripper add ll just
- Topic  8 control 12v remote pid reverse momentary switch actuators forward moving
- Topic  9 leg battery lift walker raising weight body working help using

Phrase Analysis:

- In this section I combined all post strings into one combined string to analyze the subreddits as a whole. I observed the frequency of individual tokens, as well as the frequency of bi-grams and tri-grams for each subreddit.

For datascience:

![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/datascience%20word.png)
![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/datascience%20bigram.png)
![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/datascience%20trigram.png)

For MachineLearning:

![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/machinelearning%20word.png)
![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/machielearning%20bigram.png)
![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/machinelearning%20trigram.png)

For dataanalytics:

![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/dataanalytics%20word.png)
![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/dataanalytics%20brigram.png)
![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/dataanalytics%20trigram.png)

For gamedev:

![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/gamedev%20word.png)
![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/gamedev%20bigram.png)
![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/gamedev%20trigram.png)

For robotics:

![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/robotics%20word.png)
![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/robotics%20bigram.png)
![](https://github.com/JasonSpaw/DMIR-Final-Project---Computational-Linguistics-over-Reddit-Data/blob/main/robotics%20trigram.png)

Conclusion:

- When comparing the mean sentiment scores across the subreddits, DataScience appears to have the highest compound score on average, meaning it carries the highest amount of positive sentiment, followed by gamedev and MachineLearning, while there was not as much enthusiasm in robotics.  As a whole, none of the subreddits experienced any real negativity, with most submissions primarily carrying high neutral sentiment scores meaning that these subreddits are likely more informative and a place for users to help one another with programming related issues and questions.  Topic models appear to confirm this as they seem to all depict either instructions or what would appear to be news related to that field.  This is even further confirmed when observing the most frequent words, bi-grams and tri-grams, as they are all either related to the field of study or are words, bi-grams or tri-grams that would either indicate a request for help or instructions in response to a request for help on a particular issue, along with common programming commands that might be referred to. Examples that are observed across all subreddits would be data, question, education,  _getitem, get, job, help, need, would, want, know, [would, want], [would, want, know], [try, make], [want, make, sure].  The other high frequency words and n-grams are related to the subject of that particular subreddit. For example, the subreddit datascience contained bi-grams such as [data, science], [data, scientist], [data, analyst], [Data, science].
