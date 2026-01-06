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

The funnel tracks a new user's journey from signing up to "The Mind Power" app and meaningfully consuming meditation audios.

### Primary Activation Funnel
This funnel focuses on early user engagement and activation.

1. User Awareness
   - User becomes aware of the application "The Mind Power" through marketing strategies utilized in social media presence, flyers, ads etc.
  
2. App Install
   - User proceeds to install the app after being aware of it 

3. Signup Completed
   - User proceeds to sign up with an email and password and login to their account to explore the app

4. Onboarding Completed  
   - The user completed their profile providing their details such as age, gender, what drew their interest in the app, what they wish to accomplish etc.

5. First Session Started  
   - After completing their profile, the user proceeds to choose a meditation sound based on their interest and proceeds to star a session.

6. Session Completed  
   - When a user completes one session after starting it.
  
7. Repeat engagement
   - Identifying when the user forms a habit and returns back to the app to use the features
  
8. Subscription
   - Based on the user's repeated usage user is prompted to unlock additional features if they subscribed

This funnel provides insights on user behavior on identifying when a user disengages with the app from sign-up, activation to subscribing to the app.


## Retention Definition

Retension gives us an idea of weather a user has completed at least one meditation session within a time range such as Day 1, Day 7-13, Day 30-36.

### Retention Windows
- Day 1 (D1): User completes a session 1 day after signup
- Day 7 (D7): User completes a session between days 7-13 after signup
- Day 30 (D30): User completes a session between 30-36 after signup

### Notes
- Retention can be estimated based on the user's sign up date by grouping them into categories using cohort analysis.


## Assumptions & Limitations

### Assumptions

- The data in this project is generated to reflect user behavior patterns in the 'The Mind Power' app.
- Timezones are normalized to UTC.
- Each session has a unique session_id.
- Each user has a unique user_id.
- Project is focused on observing user behavioral analytics.

### Limitations

- This is a simulated data using python and not a real-word/public data.
- The main focus of the project is on short-term retention.
