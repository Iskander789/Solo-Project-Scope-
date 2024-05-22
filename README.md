# Movie Club App (Name TBD)

The Movie Club App is designed to bring movie enthusiasts together by allowing users to share their reactions and reviews of films they agree to watch, similar to a book club. This app facilitates the creation of a virtual movie club where members can discuss movies, rate them, and leave comments. The app uses modern web development technologies and follows best practices for a beginner programmer's project.

## Objectives

- Allow users to create and join movie clubs.
- Enable members to propose and vote on movies to watch.
- Provide a platform for members to post reviews and discuss movies.
- Implement a user-friendly interface for seamless interaction.

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
- `axios`: ^0.21.1

### Development Tools

- `@vitejs/plugin-react`: ^4.2.1
- `cypress`: ^13.6.0
- `nodemon`: ^2.0.4
- `start-server-and-test`: ^2.0.3
- `vite`: ^5.0.10

## Features

### User Authentication

- Sign up and login functionality.
- Password recovery.

### Movie Club Management

- Create, join, and leave movie clubs.
- Invite users to clubs.

### Movie Proposals and Voting

- Propose movies for the club to watch.
- Vote on proposed movies.
- Schedule movie watching events.

### Movie Reviews and Discussions

- Post reviews and rate movies.
- Comment on reviews and participate in discussions.

### User Profile

- View and edit user profiles.
- Track watched movies and ratings.

### Notifications

- Notify users of new movie proposals, votes, and comments.

## Technical Stack

### Frontend

- React for building the user interface.
- Redux for state management.
- React Router for navigation.
- Axios for making HTTP requests.

### Backend

- Express.js for handling server-side logic.
- PostgreSQL for database management.

### Development

- Vite for build tool and development server.
- Cypress for end-to-end testing.
- Nodemon for automatically restarting the server.
- Vitest for unit testing.

## Architecture

### Client-Server Communication

- RESTful API endpoints using Express.
- Client-side makes API calls using Axios.

### State Management

- Global state managed with Redux.
- Side effects handled with Redux Saga.

## Development Workflow

### Set up the server

1. Create routes, controllers, and models.
2. Set up PostgreSQL database and configure connection.

### Build the frontend

1. Create React components and containers.
2. Implement Redux for state management.
3. Set up routing with React Router.

### Integrate frontend and backend

1. Use Axios to make API calls from React components to Express server.

### Deploy

1. Build the application using Vite.
2. Deploy to a cloud provider or web server.

---

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.

## Acknowledgements

Credits to those who have helped and inspired the project.
