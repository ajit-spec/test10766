# MEAN Stack Application

## Overview
This is a full-stack JavaScript application built using the MEAN stack:
- **M**ongoDB: NoSQL database
- **E**xpress.js: Web application framework for Node.js
- **A**ngular: Front-end framework
- **N**ode.js: JavaScript runtime environment

## Features
- User authentication and authorization
- RESTful API
- CRUD operations
- Responsive UI

## Prerequisites
- Node.js (v14+)
- npm (v6+)
- MongoDB (v4+)
- Angular CLI

## Installation

### Clone the repository
```bash
git clone <repository-url>
cd <project-folder>
```

### Install dependencies
```bash
# Install server dependencies
npm install

# Install client dependencies
cd client
npm install
```

### Configure environment variables
Create a `.env` file in the root directory:
```
PORT=3000
MONGODB_URI=mongodb://localhost:27017/meanapp
JWT_SECRET=your_jwt_secret
```

## Running the Application

### Development mode
```bash
# Run server (from root directory)
npm run dev

# Run Angular client (in a separate terminal)
cd client
ng serve
```

Access the application at `http://localhost:4200/`

### Production mode
```bash
# Build Angular client
cd client
ng build --prod

# Run server (from root directory)
npm start
```

## Project Structure
```
├── client/                 # Angular frontend
│   ├── src/
│   │   ├── app/
│   │   ├── assets/
│   │   └── environments/
│   ├── angular.json
│   └── package.json
├── server/                 # Node.js/Express backend
│   ├── config/             # Configuration files
│   ├── controllers/        # Request handlers
│   ├── middleware/         # Custom middleware
│   ├── models/             # Mongoose models
│   └── routes/             # API routes
├── .env                    # Environment variables
├── .gitignore
├── package.json
└── README.md
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login and get token

### Users
- `GET /api/users` - Get all users (admin only)
- `GET /api/users/:id` - Get user by ID
- `PUT /api/users/:id` - Update user
- `DELETE /api/users/:id` - Delete user

### Items (Example resource)
- `GET /api/items` - Get all items
- `GET /api/items/:id` - Get item by ID
- `POST /api/items` - Create a new item
- `PUT /api/items/:id` - Update item
- `DELETE /api/items/:id` - Delete item

## Testing
```bash
# Run backend tests
npm test

# Run frontend tests
cd client
ng test
```

## Deployment
- The Angular client can be deployed to services like Netlify, Vercel, or Firebase Hosting
- The Node.js backend can be deployed to Heroku, DigitalOcean, AWS, etc.
- MongoDB can be hosted on MongoDB Atlas

## Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the LICENSE file for details
