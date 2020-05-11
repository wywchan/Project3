## Project 3: NLP and Reddit Classification

### Problem Statement

This project is In the interest of improving and updating public education for things people feel they should know but are too embarrassed to ask.

We will build a classification model that can take inputs and determine if a topic is worth building up resources for by comparing posts in ‘TooAfraidToAsk’ (which is generally viewed as a more serious forum) vs ‘NoStupidQuestions’ (which is based off of questions that are just curiosities).

### Executive Summary

The model allowed us to gain some valuable insight despite not having a high accuracy score. The two subreddits are very similar in that they welcome questions on a variety of topics. That the model was not able to draw a line down the middle to separate posts from each is not completely surprising.

Where we found success was in identifying what the model prioritized as keywords that occur most frequently. These are those relating to health and family situations. If there is a change to improving public education, it could relate to providing more support to these sorts of matters.

---

### Data Dictionary

|Feature|Type|Description|
|---|---|---|
|subreddit|int64|The subreddit that the post originated from|
|selftext|object|The content of the post. If the selftext was blank, the post title was appended in its place|
|title|object|The title of the reddit post|
|selftext_stem|object|The stemmed version of selftext|
|title_stem|object|The stemmed version of title|
|title_selftxt|object|The concatenation of selftext_stem and title_stem|

#### Provided Data

Provided datasets:

- [Cleaned Posts Extracted from Reddit](./posts_clean.csv)

---

### Conclusions and Recommendations
While the optimal model's predictive accuracy was not very high at 68%, we are able to make a few conclusions and recommendations still.

The model is too sensitive in that it rejects posts to 'NoStupidQuestions' when they are in fact 'TooAfraidToAsk'. Conversely, it does well in classifying posts to 'NoStupidQuestions' because of this. This is also indicative of the dataset not having clear cut verbage/subjects that separate the two subreddits.

However, the main topics that occur most frequently relate to either medical/health conditions and family relationship questions. This indicates that these are the words that influence the model to classify into 'TooAfraidToAsk' the most. If we were to choose an area to invest resources in, it would be towards these two subjects.

Support initiatives could include:
- expansion and promotion of TeleHealth (perhaps an online version)
- online relationship helpline and counselling (like 7cups, theSpark, or ginger.io)
- creation/support/expansion of family health conversations (as per study from Nursing Research & Practice journal)<sup>1</sup>
- directly adding to curriculum coping methods and tactics for discussion of sensitive matters

<sup>1</sup>https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3995177/
