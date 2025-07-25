# MERN Bug Tracker

A full-stack bug tracking application built with the MERN stack (MongoDB, Express, React, Node.js). This app allows users to register, log in, create and manage bug reports, and collaborate in rooms.

## Features
- User authentication (register/login)
- Create, edit, and delete bug reports
- Personal and room-based bug tracking
- Pagination and responsive UI
- RESTful API backend
- Comprehensive testing for backend

---

## Installation & Running the Project

### Prerequisites
- [Node.js](https://nodejs.org/) (v16+ recommended)
- [MongoDB](https://www.mongodb.com/) (local or Atlas)
- [pnpm](https://pnpm.io/) (or use npm/yarn, but pnpm is recommended)

### 1. Clone the repository
```sh
git clone <repo-url>
cd mern-bug-tracker
```

### 2. Install dependencies
#### Server
```sh
cd server
pnpm install
```
#### Client
```sh
cd ../client
pnpm install
```

### 3. Set up environment variables
- Create a `.env` file in the `server/` directory with the following:
  ```env
  MONGO_URI=<your-mongodb-uri>
  JWT_SECRET=<your-secret>
  PORT=5000
  ```

### 4. Start the development servers
#### Server (API)
```sh
cd server
pnpm run dev
```
#### Client (React)
```sh
cd client
pnpm run dev
```
- The client will run on [http://localhost:5173](http://localhost:5173)
- The server will run on [http://localhost:5000](http://localhost:5000)

---

## Running Tests

### Backend Tests
- Tests are written using [Jest](https://jestjs.io/).
- To run all backend tests:

```sh
cd server
pnpm test
```

- Test files are located in `server/tests/`.
- Coverage reports are generated by Jest and can be viewed in the terminal after running tests.

### Debugging Techniques
- Use `console.log` statements in both client and server code for quick debugging.
- For backend, you can use [VS Code Debugger](https://code.visualstudio.com/docs/nodejs/nodejs-debugging) with breakpoints in the `server/` folder.
- For frontend, use browser DevTools (Console, Network tab) to inspect API calls and UI state.
- Error boundaries and error messages are displayed in the UI for easier troubleshooting.

---

## Testing Approach & Coverage

- **Unit & Integration Tests:**
  - The backend (`server/`) includes unit and integration tests for routes, models, and utility functions.
  - Tests cover authentication, bug CRUD operations, room management, and validation logic.
- **Test Coverage:**
  - The test suite aims for high coverage of critical backend logic, including edge cases and error handling.
  - Coverage includes:
    - API endpoints (auth, bugs, rooms)
    - Data validation (e.g., `validateBug.js`)
    - Middleware (auth, error handling)
- **Manual Testing:**
  - The frontend is manually tested for all user flows: registration, login, bug creation/editing/deletion, room joining/creation, and pagination.
- **Continuous Improvement:**
  - New features and bug fixes are accompanied by new or updated tests to maintain reliability.

---

## Contributing
Pull requests are welcome! Please add tests for new features and ensure all tests pass before submitting.

---

## License
MIT
