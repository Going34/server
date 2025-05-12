# Moment Gallery Server

This is the backend server for the Moment Gallery application, providing Socket.io functionality for video calls and other real-time features.

## Features

- Socket.io server for real-time communication
- Video call functionality
- Room management for video calls
- User presence tracking

## Getting Started

### Prerequisites

- Node.js 18 or later
- npm or yarn

### Installation

1. Clone the repository
2. Install dependencies:
   ```
   npm install
   ```
3. Start the server:
   ```
   npm start
   ```

### Environment Variables

- `PORT`: The port on which the server will run (default: 5000)
- `ALLOWED_ORIGINS`: Comma-separated list of allowed origins for CORS (default: "*")

## Docker

You can also run the server using Docker:

```
docker build -t moment-gallery-server .
docker run -p 5000:5000 moment-gallery-server
```

## API Endpoints

- `GET /`: Simple endpoint to verify the server is running
- `GET /health`: Health check endpoint

## Socket.io Events

### Client to Server

- `joinRoom`: Join a room
- `getUsersInRoom`: Get users in a room
- `authenticate`: Authenticate a user
- `connectToPartner`: Connect to a partner
- `callUser`: Call a user
- `answerCall`: Answer a call
- `rejectCall`: Reject a call
- `callEnded`: End a call

### Server to Client

- `me`: Send the socket ID to the client
- `usersInRoom`: Send the list of users in a room
- `userOnline`: Notify that a user is online
- `partnerFound`: Notify that a partner has been found
- `partnerNotFound`: Notify that a partner has not been found
- `userOffline`: Notify that a user is offline
- `partnerDisconnected`: Notify that a partner has disconnected
- `callUser`: Notify of an incoming call
- `callAccepted`: Notify that a call has been accepted
- `callRejected`: Notify that a call has been rejected
- `callEnded`: Notify that a call has ended
