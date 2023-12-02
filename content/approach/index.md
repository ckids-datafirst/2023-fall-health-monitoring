---
title: Approach
summary: Data science methodology used to address the problem, including data preprocessing steps, exploratory data analysis, feature engineering techniques, machine learning models, and evaluation metrics.
date: "2018-06-28T00:00:00Z"
editable: true
share: true
---


## Data Quality

The main issue with data quality can be attributed to ensuring that each patient has realistic health values charted for each simulated session at the bidet. An example of this, which we came across early in the process, was that some of our patients had temperatures in the low 60s/70s or in the 120s/130s range. At first, we saw it as a success that we were able to simulate abnormalities and sustained health data, but soon realized that the temperature values we were recording would mean that the patient was dead. To fix this small error, we consulted with our mentor, Dr. Mathura, about his insights from the medical field and looked at standard ranges for each health metric published by health officials.

## Data Preprocessing

Data processing was mainly done using Python's Pandas. Due to the initial data we collected on Kaggle, the data was in a CSV format that was read into a dataframe using Pandas. From there, we constructed the baseline data for the initial 6000 patients, given each piece of data that we had collected from Kaggle, and filling in the blanks with data that was in the normal range found within the individual health metrics. After we had the initial baseline for each patient, we simulated 28 days and two bathroom sessions for each patient to expand our dataset.

When simulating the data for each patient, we started with their baseline entry in the data frame and added/subtracted the standard range at which one person should change in that particular health metric. This measure would continue for the rest of the entries using the previous one as the new baseline to determine future results. Within this effort, we also wanted to include abnormalities that we could potentially flag later in the process to detect heart failure. We achieved this by adding a 7% chance (using a randomizer) of abnormal change that would deviate from the normal standard range and double the range of an increase/decrease that can happen. An example of this in practice that I can share is weight. From our studies and talks with our mentors, the average person will experience a daily +7/-7 weight change, which is normal and expected. This would happen 93% of the time; however, the 7% chance would allow for a person to have a +14/-14 weight change, which would be abnormal. This way, while not with the same exact numbers, can be seen for each health metric.

## Exploratory Data Analysis (EDA)

The first way that we explored the data was by charting the differences with patients across the different health metrics over days, weeks, and the month( we did this using matplotlib) to guarantee that we had normal and abnormal data mixed in that we can use to flag for heart failure.

The main goal of this project was to detect heart failure, and with certainty that patient data wasn't static and not drastically abnormal (people can slip up from time to time), we charted forward to flagging health metrics that could lead to heart failure. With the fully completed database, the way that we flagged health metrics for each patient was by using both a personal and public range to determine if the metric is normal, risky (yellow), or dangerous (red). For the personal range, we added the range of all the entries of the health metric for that patient, and for the public range, we used the normal/healthy ranges given by health experts. We looked at how much the patient deviated from both ranges, and if it was less than one, it was normal/healthy. If it was between 1 and 3, then it would be categorized as risky and given a yellow flag or warning. Finally, if it was above 3, then it would be flagged with red, and the patient would have a dangerous health metric.

