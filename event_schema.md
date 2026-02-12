# Event Schema

This document defines the structure of the event-level dataset used for funnel and retention analysis.

## Table: events

Each row represents a single user event.

| Column Name      | Description |
|------------------|-------------|
| event_id         | Unique identifier for each event |
| user_id          | Unique identifier for each user |
| event_name       | Name of the event |
| event_timestamp  | Timestamp when the event occurred |
| event_date       | Date of the event |
| platform         | Platform used (iOS, Android, Web) |
| country          | User country |
| session_id       | Identifier for user session |

## Event Types

The dataset includes the following events:

- app_install  
- sign_up  
- onboarding_completed  
- session_started  
- session_completed  
- subscription_started  

These events represent key stages of the user journey and will be used to compute funnel conversion and retention metrics.
