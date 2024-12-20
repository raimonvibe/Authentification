# Authentication System

A secure authentication system built with Node.js and Express that allows users to register, login, and share secrets anonymously. This application provides a simple interface for user registration and authentication, with encrypted password storage using MongoDB.

## Features

- User Registration and Login
- Secure Password Storage with Encryption
- MongoDB Database Integration
- Clean and Responsive UI using Bootstrap
- EJS Templating

## Prerequisites

- Node.js
- MongoDB (running locally on port 27017)
- npm (Node Package Manager)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/raimonvibe/Authentification.git
cd Authentification
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory with your secret key:
```
SECRET=your_secret_key_here
```

4. Ensure MongoDB is running locally on port 27017

5. Start the application:
```bash
node app.js
```

The server will start on `http://localhost:3000`

## Project Structure

```
├── app.js              # Main application file with routes and MongoDB setup
├── package.json        # Project dependencies
├── public/
│   └── css/
│       └── styles.css  # Custom styling
└── views/
    ├── home.ejs       # Landing page
    ├── login.ejs      # Login form
    ├── register.ejs   # Registration form
    ├── secrets.ejs    # Protected secrets page
    └── partials/      # Template partials
        ├── header.ejs
        └── footer.ejs
```

## Dependencies

The project uses the following npm packages:
- `express` (^4.18.1): Web framework
- `mongoose` (^6.3.4): MongoDB object modeling
- `ejs` (^3.1.8): Templating engine
- `dotenv` (^16.0.1): Environment variable management
- `body-parser` (^1.20.0): Request parsing
- `mongoose-encryption` (^2.1.2): Database encryption

## Usage

1. Visit the home page at `http://localhost:3000`
2. Click "Register" to create a new account or "Login" if you already have one
3. After authentication, you'll be able to view and submit secrets

## Security

The application implements basic security features:
- Password encryption using mongoose-encryption
- Environment variables for sensitive data
- Secure session handling
