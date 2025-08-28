# Accounts Microservice

A robust, production-ready microservice for managing account operations built with Node.js and Express.

## 🚀 Technologies Used

### Core Framework
- **Node.js** - JavaScript runtime environment
- **Express.js 5.1.0** - Fast, unopinionated web framework for Node.js

### Database & ODM
- **MongoDB** - NoSQL document database
- **Mongoose 8.18.0** - MongoDB object modeling tool with schema validation

### Validation & Configuration
- **Joi 18.0.1** - Schema description language and validator for JavaScript objects
- **dotenv 17.2.1** - Environment variable management

### Architecture Pattern
- **MVC (Model-View-Controller)** - Clean separation of concerns
- **RESTful API Design** - Standardized API endpoints
- **Microservice Architecture** - Independent, focused service

## 🏗️ Project Structure

```
accounts-microservice/
├── configs/                 # Environment configuration files
├── src/
│   ├── app.js              # Express application setup
│   ├── index.js            # Server entry point
│   ├── config/
│   │   └── config.js       # Configuration management with validation
│   ├── controllers/
│   │   └── account.js      # Business logic handlers
│   ├── db/
│   │   └── index.js        # Database connection management
│   ├── middlewares/
│   │   └── validate.js     # Request validation middleware
│   ├── models/
│   │   └── account.js      # Mongoose schema and model
│   ├── routes/
│   │   └── v1/             # API versioning
│   │       └── accounts/   # Account-specific routes
│   ├── services/
│   │   └── account.js      # Business logic layer
│   └── validation/
│       └── account.js      # Joi validation schemas
├── package.json
└── README.md
```

## 🔧 Key Features

### 1. **Environment Configuration Management**
- Centralized configuration with environment variable validation
- Joi schema validation for configuration values
- Support for multiple environment files

### 2. **Database Layer**
- MongoDB connection with automatic retry mechanism
- Mongoose ODM with optimistic concurrency control
- Proper connection lifecycle management

### 3. **Data Validation**
- Request body and parameter validation using Joi
- MongoDB ObjectId validation
- Comprehensive validation schemas for all operations

### 4. **API Design**
- RESTful API endpoints
- API versioning (v1)
- Standardized error handling

### 5. **Account Management**
- Create, read, update, and delete account operations
- Account types: root and sub accounts
- Account status management (new, active, inactive, blocked)

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB instance
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd account-microservice
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
   Create a `.env` file in the `configs/` directory:
   ```env
   PORT=3000
   MONGODB_URL=mongodb://localhost:27017/accounts_db
   ```

4. **Start the service**
   ```bash
   npm start
   ```

## 📡 API Endpoints

### Account Operations
- `POST /v1/accounts` - Create a new account
- `GET /v1/accounts/:id` - Retrieve account by ID
- `PUT /v1/accounts/:id` - Update account
- `DELETE /v1/accounts/:id` - Delete account

## 🛠️ Development

### Scripts
- `npm start` - Start the application
- `npm test` - Run tests (to be implemented)

### Code Quality
- Consistent code structure following MVC pattern
- Input validation on all endpoints
- Proper error handling and logging
- Environment-based configuration

## 🔒 Security Features

- Input validation and sanitization
- MongoDB injection protection through Mongoose
- Environment variable management
- Proper error handling without information leakage

## 📊 Monitoring & Logging

- Server startup and shutdown logging
- Database connection status logging
- Unhandled error logging
- Graceful server shutdown handling

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📝 License

This project is licensed under the ISC License.

## 🆘 Support

For support and questions, please open an issue in the repository or contact the development team.

---

**Built with ❤️ using Node.js, Express, and MongoDB**
