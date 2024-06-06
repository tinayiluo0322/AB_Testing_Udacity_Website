# A/B Testing the Udacity Website

## Introduction

In this repository, we analyze data on user behavior from an A/B test conducted by Udacity, the online education company. The goal of the test was to improve the onboarding process on Udacity's site. By comparing user behaviors between those exposed to the new onboarding process and those who experienced the original process, we aim to estimate the effect of the proposed changes.

Udacity's A/B test is a type of randomized experiment where a portion of users are randomly selected to see a new version of the site. This allows analysts to compare the behaviors of users who see the new design with those who see the original design, thereby estimating the impact of the new design on user engagement and retention.

## Udacity's Test Description

The test [is described by Udacity as follows](https://www.kaggle.com/tammyrotem/ab-tests-with-python/notebook):

### Current Conditions Before Change

- **Start Free Trial**: When a student clicks "start free trial", they are asked to enter their credit card information. They are then enrolled in a free trial for the paid version of the course. After 14 days, they are automatically charged unless they cancel first.
- **Access Course Materials**: When a student clicks "access course materials", they can view videos and take quizzes for free but do not receive coaching support, a verified certificate, or feedback on their final project.

### Description of Experimented Change

- **Start Free Trial**: In the experiment, if a student clicks "start free trial", they are asked how much time they have available to devote to the course.
  - If the student indicates 5 or more hours per week, they proceed through the usual checkout process.
  - If the student indicates fewer than 5 hours per week, a message appears suggesting that Udacity courses typically require a greater time commitment for successful completion and that the student might prefer to access the course materials for free.
  - At this point, the student has the option to either continue enrolling in the free trial or access the course materials for free instead. This [screenshot](images/udacity_checkyoureready.png) shows what the experiment looks like.

### Udacity's Hypothesis

Udacity hoped that this change would set clearer expectations for students upfront, thus reducing the number of frustrated students who leave the free trial because they didn't have enough time. The goal was to achieve this without significantly reducing the number of students who continue past the free trial and eventually complete the course. If successful, this would improve the overall student experience and optimize coaches' capacity to support students who are likely to complete the course.

## Data and Analysis

### Dataset

The dataset provided by Udacity includes:
- User interactions with the onboarding process.
- User engagement metrics such as course completion rates and trial continuation rates.

### Analysis Approach

1. **Data Cleaning and Preparation**: 
   - Preprocessing the dataset to handle missing values and outliers.
   - Feature engineering to create relevant variables for analysis.

2. **Exploratory Data Analysis (EDA)**: 
   - Visualizing user behavior patterns.
   - Comparing engagement metrics between the control group and the treatment group.

3. **Statistical Analysis**:
   - Applying hypothesis testing to determine if there are significant differences in user behaviors between the two groups.
   - Calculating metrics such as conversion rates, engagement duration, and trial continuation rates.

4. **Results Interpretation**:
   - Interpreting the statistical significance and practical implications of the results.
   - Discussing the potential impact of the changes on Udacity's business objectives.

## Resources

- [Original writeup by Udacity](https://www.kaggle.com/tammyrotem/ab-tests-with-python/notebook)
- [Udacity's A/B Testing course](https://www.udacity.com/course/ab-testing--ud257)

## Conclusion

This repository provides a comprehensive analysis of Udacity's A/B test aimed at improving their onboarding process. By following the steps outlined in this README, you can replicate the analysis and gain insights into the effectiveness of the proposed changes. The results of this analysis can help Udacity make data-driven decisions to enhance user experience and optimize resource allocation.

## License

The dataset and analysis are provided under the Apache open-source license.
