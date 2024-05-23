# Movie Club App

## Objectives

- Allow users to create and join movie clubs.
- Limit clubs to a maximum of four members to encourage in-depth discussions.
- Schedule regular movie viewings every four weeks.
- Facilitate movie discussions and ratings on a message board.
- Integrate with The Movie Database (TMDb) to fetch movie details.
- Implement email reminders for scheduled movie viewings and discussions.

## Dependencies

### Frontend

- `react`: ^18.2.0
- `react-dom`: ^18.2.0
- `react-redux`: ^7.2.2
- `react-router-dom`: ^5.3.4
- `redux`: ^4.0.5
- `redux-logger`: ^3.0.6
- `redux-saga`: ^1.1.3

### Backend

- `express`: ^4.18.2
- `pg`: ^8.2.1

### Middleware

- `axios`: ^0.21.1

### Build Tool

- `vite`: ^5.0.10

## Core Features

1. **User Authentication**
   - **Registration:** Users can create an account.
   - **Login:** Users can log in to their account.
   - **Authorization:** Access to clubs and movie discussions is restricted to logged-in users.

2. **Club Management**
   - **Create Club:** Users can create a new club and invite up to three other members.
   - **Join Club:** Users can join existing clubs.

3. **Movie Selection and Scheduling**
   - **Movie Selector Rotation:** The person who creates the club selects the first movie. The selector role rotates through the group.
   - **Movie Database Integration:** Integration with TMDb to fetch and display movie details.

4. **Discussion and Rating**
   - **Message Board:** A discussion board for members to discuss the movie.
   - **Rating System:** Members can rate the movie after watching it.

5. **Notifications**
   - **Email Reminders:** Schedule function to send email reminders for movie watching and discussion deadlines.

## Stretch Goals

1. **Advanced Scheduling**
   - **Calendar Integration:** Integration with Google Calendar for scheduling movie nights and discussions.
   - **Push Notifications:** In-app notifications for upcoming movie nights and discussion deadlines.

2. **Enhanced User Interaction**
   - **Private Messaging:** Direct messaging between club members.
   - **Polls and Surveys:** Create polls for future movie suggestions or club decisions.
   - **Achievements and Badges:** Gamification elements for active participation.

3. **Mobile App**
   - **React Native Version:** Develop a mobile version of the app for iOS and Android.

4. **Additional Features**
   - **Resource Sharing:** Share links, articles, and other resources related to the movie.
   - **Activity Feed:** A feed displaying recent activities and updates within the club.
   - **Public/Private Clubs:** Option to make clubs public or private.

## Wireframes
(To be added)
- **Login/Registration Page:**
  - Features: User registration form, login form, forgot password option.
- **Dashboard:**
  - Features: List of joined clubs, option to create a new club, notifications.
- **Club Page:**
  - Features: Club details, list of members, current movie details, discussion board.
- **Movie Selection Page:**
  - Features: Movie search, display movie details, select movie button.
- **Discussion Page:**
  - Features: Discussion threads, reply option, rating system.

## Entity Relationship Diagram (ERD)
(To be added)
- **User Table:**
  - id (Primary Key)
  - username
  - email
  - password (hashed)
- **Club Table:**
  - id (Primary Key)
  - name
  - creator_id (Foreign Key)
- **Membership Table:**
  - user_id (Foreign Key)
  - club_id (Foreign Key)
- **Movie Table:**
  - id (Primary Key)
  - tmdb_id
  - title
  - description
- **Discussion Table:**
  - id (Primary Key)
  - club_id (Foreign Key)
  - user_id (Foreign Key)
  - movie_id (Foreign Key)
  - content
  - created_at
- **Rating Table:**
  - id (Primary Key)
  - user_id (Foreign Key)
  - movie_id (Foreign Key)
  - rating
  - created_at

## Feature Descriptions
- **User Authentication:**
  - Users can register with their email and password. Passwords are hashed for security. Logged-in users can create or join clubs and participate in discussions.
  
- **Club Management:**
  - Users can create a new club by providing a club name. The user who creates the club becomes the first movie selector. Clubs are limited to four members to ensure manageable discussions. Users can search for and join existing clubs until the membership limit is reached.

- **Movie Selection and Scheduling:**
  - The first movie is selected by the club creator. Subsequent selections rotate among club members. Integration with The Movie Database (TMDb) allows users to search for movies and fetch details like title, description, and poster. Each movie viewing is scheduled to occur every four weeks, with automatic reminders sent to all club members.

- **Discussion and Rating:**
  - After watching the selected movie, members can discuss it on the club’s message board. Each discussion thread is tied to a specific movie. Members can post comments and replies, and rate the movie on a scale of 1 to 5 stars. Ratings are aggregated to provide an average club rating for each movie.

- **Notifications:**
  - Email reminders are sent out to members before the scheduled movie viewing and discussion deadlines. This feature ensures that members are reminded of upcoming events without having to manually check the app.

## Stretch Goals

1. **Advanced Scheduling:**
   - **Calendar Integration:** Allow users to sync movie nights and discussions with their Google Calendar, ensuring they receive reminders and notifications on their preferred calendar app.
   - **Push Notifications:** Implement in-app notifications to alert users of upcoming events, new messages on the discussion board, and other important updates.

2. **Enhanced User Interaction:**
   - **Private Messaging:** Enable direct messaging between club members for private discussions and planning.
   - **Polls and Surveys:** Allow club members to create polls for suggesting future movies or making club-related decisions.
   - **Achievements and Badges:** Introduce gamification by awarding badges and achievements for milestones such as consistent participation, hosting movie nights, and providing insightful reviews.

3. **Mobile App:**
   - **React Native Version:** Develop a mobile app using React Native, allowing users to access the Movie Club app on both iOS and Android devices. The mobile app will provide the same core features as the web app, ensuring a seamless experience across platforms.

4. **Additional Features:**
   - **Resource Sharing:** Provide a space for members to share links, articles, and other resources related to the movies they watch.
   - **Activity Feed:** Implement a feed displaying recent activities within the club, such as new discussions, ratings, and movie selections.
   - **Public/Private Clubs:** Give users the option to make their clubs public (open to anyone) or private (invitation-only), providing more flexibility in how they manage their movie clubs.

## Conclusion
The Movie Club app aims to recreate the social and interactive experience of a book club for movie enthusiasts. By leveraging modern web technologies and integrating with The Movie Database, the app provides a robust platform for users to discover, watch, and discuss movies in a collaborative environment. The inclusion of stretch goals ensures that the app can evolve to meet the needs of its users, providing additional features and enhancements as development progresses.
