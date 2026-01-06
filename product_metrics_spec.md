# Product & Metrics Specification

## Product Overview
- This is a wellness app called 'The Mind Power', which offers mindul meditation audios for different areas of trobles such as Depression, Anxiety or for just having a better quality of life. 
- This app is built for people of ages 18 and above all over the globe. 
- This is a 7 day free trail app and then people would have to subscribe to get all the features.

## Business Objective
- Primary goal is to improve 30-day retention

## Key User Events
- signup_completed - When a user registers with an email and password
- onboarding_completed - After signup, a user completes his/her profile to complete onboarding
- session_started - When a user utilizes a service within the app, records the session start time
- session_completed - Records the user's session end time.
- session_ID - Unique identifier for each of the sessions
- subscription_started - Time when the user subscribes after making a payment to a service

## Activation Definition
- When a user completes at least one session within 3 days of signup

## Funnel Definitions

The primary user funnel tracks how new users progress from signup to experiencing core product value and, optionally, converting to a paid subscription.

### Primary Activation Funnel
This funnel focuses on early user engagement and activation.

1. Signup Completed  
   - Event: `signup_completed`
   - Definition: User successfully creates an account.

2. Onboarding Completed  
   - Event: `onboarding_completed`
   - Definition: User finishes the initial onboarding flow.

3. First Session Started  
   - Event: `session_started`
   - Definition: User starts their first wellness session.

4. Session Completed  
   - Event: `session_completed`
   - Definition: User completes at least one full session.
   - This step is considered the point of activation.

### Paid Conversion Funnel (Secondary)
This funnel tracks conversion to a paid subscription among engaged users.

1. Activated User  
   - Definition: User has completed at least one session.

2. Subscription Started  
   - Event: `subscription_started`
   - Definition: User begins a paid subscription.


## Retention Definition

Retention is measured using cohort-based analysis, where users are grouped by their signup date.

A user is considered retained on Day N if they complete at least one wellness session on Day N after signup.

### Retention Windows
- Day 1 (D1): User completes a session 1 day after signup
- Day 7 (D7): User completes a session 7 days after signup
- Day 30 (D30): User completes a session 30 days after signup

### Notes
- Retention is measured at the user level.
- Multiple sessions on the same day count as a single retained user.
- Passive activity (e.g., app opens without session activity) is not considered retention.


## Assumptions & Limitations

- The dataset used in this project is simulated to reflect realistic user behavior patterns in a freemium wellness app.
- User behavior probabilities (e.g., onboarding completion, session completion, retention) are based on reasonable assumptions rather than real production data.
- The analysis assumes a single primary user journey and does not account for multiple personas or advanced segmentation.
- Timezones are normalized, and all events are treated as occurring in a single timezone.
- The project focuses on behavioral analytics (funnels and retention) and does not include financial metrics such as revenue, LTV, or churn modeling.
