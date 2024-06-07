# Design and Implementation

## Frontend

StepQuest is developed in Kotlin, targeted towards Android phone users. Its architecture uses ViewModels for efficient, maintainable interaction with the backend. The user interface is designed using the Jetpack Compose framework, allowing for dynamic UI rendering.
 
The app is divided into three main screens:
- **Home screen:** this screen gives the user access to their profile page, notifications, current challenges and to the global and friend score leaderboards.
- **Map:** this screen, implemented with the Google Maps API, shows the user's location. From there, they can display and follow nearby routes, or create their own route.
- **Progression page:** this screen shows the user's current daily and weekly step counts as well as their step goals, and allows them to modify said goals.

## Backend
  
**ViewModels:** each screen is associated to a ViewModel handling the backend logic and application functionalities.  
**Database interactions:** user data is stored in a Firebase Realtime database, allowing for efficient data fetching.  
**Data caching:** some data is directly cached in the application to allow users to use it when offline. 

## Data Model

Various information is collected to enable the app's functionalities, including the user's:
- **Login information:** using Firebase authentication, users can easily create accounts.
- **Created routes,**  shared to all nearby users.
- **Step counts,** both daily and weekly.
- **Friends list**

Additionally, several pieces of related data are stored, such as pending friend and challenge requests or challenge progression.

Data is stored in a Firebase Realtime database. It is organised in six collections:
- **Challenges:** allows an easy, shared access to challenges for both users instead of having to duplicate it.
- **Leaderboard:** stores each user's total score.
- **Users:** stores most of the user information, except anything that might require easier access.
- **Usernames:** shortcut associating each user's username to their predetermined user ID.
- **Routes**
- **Notifications**

In addition, some data is cached in the application: it includes the user's login, created routes and step count. This allows for offline functionalities, albeit restricted.

## Security Considerations
Since user information is stored on a global database, it is important to set it up correctly so data can't be accessed or modified by unauthorized parties. Additionally, when developing functionalities related to user location, one should be careful as to not share users' positions to everyone around them.

## Infrastructure and Deployment

Since we're using a Firebase database to store data, it is important that the database is well organized and set up, especially in terms of security rules.

## Test Plan

Necessary tests can be divided into several kinds:
- **UI:** everything is displayed correctly.
- **App functionality:** all front-end features are implemented accurately and behave as expected.
- **Back-end reliability:** database reads and writes work properly.

In addition to that, some functionalities should be tested manually, because automating them can prove to be quite tricky; this is mostly the case with features using the phone's sensors, such as the map or step counter.
