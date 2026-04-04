# Product Funnel & Retention Analysis for a Wellness App

This project simulates user behavior for a freemium wellness app and analyzes how users move through the product funnel, return over time, and convert to paid subscriptions.

I built this project to practice end to end product analytics workflow using Python for data generation, SQL for analysis, and Tableau for visualization.

## Project Overview

The goal of this project was to answer two important product questions:

1. Where are users dropping off in the funnel?
2. How well does the product retain users after signup?

To answer these questions, I created a simulated event level dataset for a wellness app and analyzed user progression across key stages such as install, signup, onboarding, session activity, and subscription.

## Business Problem

Freemium products often struggle with two major challenges:

- getting users to complete onboarding and experience value
- converting engaged users into paid subscribers

This project analyzes both problems by focusing on:

- funnel conversion from install to subscription
- cumulative retention across Day 1, Day 7, and Day 30

## Dataset Design

I created two datasets for this project:

### 1. `dim_users`
A user dimension table with one row per user.  
Includes attributes such as:

- `user_id`
- `signup_ts`
- `country`
- `persona`

### 2. `fact_events`
An event table with one row per event.  
Includes the following events:

- `app_install`
- `sign_up`
- `onboarding_completed`
- `session_started`
- `session_completed`
- `subscription_started`

The event data was generated with realistic logic so that users follow a believable product journey. For example:

- all users install and sign up
- only a subset complete onboarding
- only onboarded users can generate sessions
- only users with completed sessions are eligible to subscribe

## Tools Used

- **Python** for data generation and preprocessing
- **Pandas** for dataframe manipulation
- **SQLite / SQL** for funnel and retention analysis
- **Tableau** for dashboard visualization
- **GitHub** for version control and project presentation

## Analysis Performed

### Funnel Analysis
I measured the number of distinct users who reached each stage of the product journey:

- `app_install`
- `sign_up`
- `onboarding_completed`
- `session_started`
- `subscription_started`

I then calculated:

- step to step conversion
- overall conversion from install

### Retention Analysis
Using `session_started` as the return event, I calculated cumulative:

- Day 1 retention
- Day 7 retention
- Day 30 retention

## Key Insights

- In this dataset, 100% of users who installed the app also signed up
- Nearly **49%** of users dropped off during onboarding, making it the first major friction point in the funnel
- Around **47%** of users reached the session stage, but only **9%** ultimately converted to paid
- Only about **19%** of users who started a session subscribed, showing a major gap between engagement and monetization
- Cumulative retention increased from **5.46% on Day 1** to **28.96% by Day 7** and **47.51% by Day 30**

### Product Takeaway
The biggest opportunities appear to be:

- simplifying onboarding to reduce early drop-off
- improving value delivery during the first few sessions
- introducing stronger post-session conversion triggers to increase subscription uptake

## Dashboard Preview

![Dashboard Preview](dashboard/dashboard.png)

## Repository Structure

```text
Product-Funnel-Retention-Analysis-for-a-Wellness-App/
│
├── data/
│   ├── dim_users.csv
│   ├── fact_events.csv
│   ├── funnel_metrics.csv
│   └── retention_metrics.csv
│
├── notebooks/
│   └── funnel_retention_analysis.ipynb
│
├── dashboard/
│   ├── user_funnel_retention_dashboard.twbx
│   └── dashboard.png
│
└── README.md
