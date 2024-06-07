# Functional Requirements

*Max 3 pages.*

*List the key features of the MVP precisely.*

## Step Counter
A basic step counter that tracks the user's steps. It keeps note of the date to distinguish between daily steps made, weekly steps made, and total steps. The step count can be accessed by the user on the progression page, where they can see their daily and weekly step count, which update in real time as the user is taking steps. The user can access their total step coun in the profile page.

## Friend System
Allows users to add friends and view their activity, as well as send challenges to friends to compete. Users can send and accept friend requests, view friends' step counts, and interact through challenges.

## Daily and Weekly Step Goals
Users can set and track personal daily and weekly step goals. Users can set a step goal for a day or week, and can see their progress towards this goal. Users earn points upon achieving these goals.

## Challenges
Various step-based challenges that users can compete in with friends. These challenges are intiated by a a user who send a challenge to another user in their friends list. The other user receives a notification on the app and can choose to accept the challenge. The user compete to be the first to finish the challenge, with points awarded for completion.

## Map and Route Features
Interactive map feature enabling users to create and follow routes. Users can add checkpoints to their routes with pictures of the checkpoint, so that other users can follow the route and match the same checkpoint. Users can use a search feature to search nearby routes created by other users, or search for routes in a location of their choice using the search bar. Users can start following existing routes, and earn points by doing so. App tracks progress along predefined routes, and ensures that the user followed the route without detours or shortcuts.

## Score System and Leaderboards
A comprehensive scoring system tied to user activity. Points are awarded for completing goals, challenges, and routes (Number of points depend on the number of steps of the step goal or the challenge, and the length of route). Leaderboards display rankings among friends and globally to foster a competitive spirit and reward users who try to be the most active. User can access a global leaderboard which holds the ranking of all users, or a friends leaderboard, that ranks only the user with other within his/her friends list.

*Include appropriate architectural diagrams.*

![architechture diagram](images/PRD_requirements_architecture.png)

*Describe key internal functionality.*

## Step Counter
Utilizes the mobile device's built-in step counter sensor to detect when a step is made. When a step is made, the app takes note of the date, and updates the total step count on the database, as well as the weekly and daily step counts according to the date. In offline mode the app instead simply caches this information, and saves the values from the cache to the database the next time the device is connected to the internet.

## Friend System
Interfaces with Firebase Realtime Database to manage friend requests, acceptances, and deletions. When a user first logs into StepQuest, the app request that they set the username. The database keeps track of users' names, and provides this information to the app to allow all users to search for each other by the username to add friends. When adding friends, the request is saved on the database. The app checks the database for any friend requests to add to the notification tab, and updates the database based on whether the request was accepted or denied.

## Daily and Weekly Step Goals
Interfaces with Firebase Realtime Database to check the number of steps taken both daily and weekly, and the step goals. The app updates the step goals when the user decides to set new goals. The app also gets the step count from the database, and keeps updating the value so that the user can see their progress happening in realtime. When offline, updating the step goal happens on the cache, and the cached value is added to the database the next time the device is connected to the internet.

## Challenges


## Map and Route Features
Uses GPS data and directly communicates with the Google Maps API to allow users to create, save, and follow walking routes. Provides real-time tracking on a map interface. Users can set checkpoints along routes and take pictures at these points for an enhanced interactive experience. Syncs route and checkpoint data with Firebase.

## Leaderboard System
Aggregates scores from Firebase to maintain up-to-date leaderboards. Displays rankings among friends and globally.