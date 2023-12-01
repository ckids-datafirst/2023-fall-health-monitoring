---
title: Problem and Requirements
summary: Problem and Requirements document that will drive the work to be done in the project
date: "2018-06-28T00:00:00Z"
editable: true
share: false
---

## Introduction

Technologies such as smart phones and smartwatches have provided people easy ways to monitor their health. Unfortunately, most of this data is incomplete, fragmented, and inconsistent, rendering it unusable in clinical settings. In order for the data to be clinically actionable and reimbursable as per remote therapeutic monitoring (RTM), it needs to be consistent and valid. How can we track a person’s health reliably, consistently, and unobtrusively in order to obtain clinically actionable data to provide patient-centered care? Enter the smart toilet seat, or as we like to call it, DataBidet.

## Motivation

The primary motivation for this project is to provide patient-centered care. Many clinicians aim to cater to an individual’s specific health needs when making health decisions in prescribing care (Catalyst, 2017). Patient-centered care promotes patient engagement, leading to better health outcomes and eventually, personalized medicine. Furthermore, with the DataBidet, biodata such as weight, temperature, heart rate, pulse oximetry, and blood pressure would be collected every time a person sat down to use the toilet. Unlike a smartwatch, which is easily forgotten and inaccurate, a toilet is a consistent part of everyday life.
 
## Problem for the Semester

The goal is to create a software-as-a-service data pipeline for collecting health biomarkers via an instrumented toilet seat. This clinical data management system (CDMS) will enable collecting clinical-grade, high-quality, curated, and consistent data capture that meets NIH and FDA standards of clinical utility. This system will streamline data collection, management, and reporting.

## State of the Art

Toto launched one of the first smart toilets in the early 2000s, but it was discontinued due to low demand (Baggaley, 2019). Since then, there has been interest in developing a health monitoring smart toilet from the University of Massachusetts and even Bill Gates (Spencer, 2023; Baggaley, 2019). However, no smart toilet has yet become mainstream, likely due to high costs and barriers to regulation. While our team recognizes these challenges, we are focusing on the software side of the product.
 
## Design and Approach

First, the team will generate dummy data using a variety of datasets found on Kaggle as well as looking at average human ranges while adding outliers. Once we have a comprehensive dataset comprised of multiple entries per patient with qualities that potentially could be measured through a smart toilet seat, we will upload the data to a database that is secure and HIPAA compliant. Next, we will choose one patient on which to perform analytics and create a dashboard of what a clinician might see when monitoring a patient’s data from the DataBidet.

## Use Case Scenario

DataBidet primary users would be people with chronic illnesses. People with chronic illnesses need to monitor their health more than a healthy person, so a smart toilet seat that collects reliable data would be useful for them and their doctors. Ideally, the DataBidet would be a regular gadget for people to have, similar to the Apple Watch or Fitbit. It would then be able to flag when a persons’ health changes or has any concerns. For example, if a patient suddenly gains weight, has an elevated heart rate, and has a change in blood pressure without changing their diet or exercise, it could be an indication of heart failure. The best use case scenario would be for the DataBidet to identify illnesses before people are even aware they are sick.
 
## Desired Outcomes and Benefits

The desired outcome would be to create a data collection, transmission and storage pipeline, analytics and report generation platform to produce clinically actionable, IRB and regulatorily approved, and reimbursable reports.  We would also like to create a system or platform that could collect, analyze, and distribute data to the end users. Future work would include building the actual hardware for the toilet seat and integrating the collected data with other health monitoring systems such as step counters.

## Citations

Baggaley, K. (2019, January 23). Here's how smart toilets of the future could protect your health. NBC News. https://www.nbcnews.com/mach/science/here-s-how-smart-toilets-future-could-protect-your-health-ncna961656  
Catalyst, N. E. J. M. (2017). What is patient-centered care?. NEJM Catalyst, 3(1)  
https://www.kaggle.com/datasets/burnoutminer/heights-and-weights-dataset  
https://www.kaggle.com/datasets/laavanya/human-stress-detection-in-and-through-sleep/  
Spencer, S.E.W. (2023, June 20). UMass Chan digital medicine study uses smart toilet seat to monitor heart health. UMass Chan Medical School. https://www.umassmed.edu/news/news-archives/2023/06/umass-chan-digital-medicine-study-uses-smart-toilet-seat-to-monitor-heart-health/
