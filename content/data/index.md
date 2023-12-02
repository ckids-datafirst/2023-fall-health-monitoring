---
title: Data Assessment
summary: Data Assessment Document that gives an overview of the data used for the project.

date: "2018-06-28T00:00:00Z"
editable: true
share: true
---

## Introduction

Our initial dataset for this proof of concept was acquired from Kaggle. This data includes height, weight and pulse oximetry. We synthesized the rest of the attributes (blood pressure, heart rate, temperature and daily calories) by looking at the global normal ranges. And then we injected some anomalies into the dataset to help with analysis. Most of the data was synthesized since biomarker data is usually private and hard to access. 

## Data Overview and Examples

Each row of the dataset represents the data collected every time one of our hypothetical patients uses the smart toilet seat. It is sorted by date and contains synthetic data for one month from 03-01-2023 to 03-28-2023 for 630 patients assuming every patient uses the toilet seat twice a day. The patient.csv dataset contains the following parameters:
-patient_id
-date
-time
-length_of_time(sec)	
-weight(lbs)	
-pulse_oximetry	
-heart_rate	
-bp_sys
-bp_dia	
-temperature

Apart from this, we also created two other datasets: 
-Patient demographic - contains information like age and sex of a patient
-Calories - to measure daily activity of a patient, this is a separate  dataset since it is collected at the end of each day, and not a irregular intervals like the other parameters


## Data Accessibility

We would like to upload our datasets to HIPAA compliant cloud database services like Amazon’s DynamoDB and S3 buckets. APIs will be used to perform CRUD operations on the data.

## Data Formats

Our data is tabular and in csv format.

## Data Challenges

The biggest challenge for our project was to synthesize data that appropriately represents the real world.We had to randomly generate biomarker values and then carefully inject anomalies.

## Data Visualizations and Highlights

Including a visualization is a simple way to show something interesting about the data.  Perhaps the visualizations could simply highlight the size, distribution, and other simple statistical characteristics of the data.


![A few entries and metrics in the dataframe for Patient 1001](assets/media/dataScreenshot.png)
