# AI Ninja App

A modern web application built with React, featuring Google Authentication using Firebase and a clean UI with Tailwind CSS.

## Features

- 🔐 Google Single Sign-On (SSO) Authentication
- 🛡️ Protected Routes
- 🎨 Modern UI with Tailwind CSS
- 🔄 Automatic Route Redirection
- 📱 Responsive Design

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v14 or higher)
- npm or yarn
- A Firebase project with Google Authentication enabled

## Getting Started

1. Clone the repository:
```bash
git clone [your-repo-url]
cd ai-ninja-1/client
```

2. Install dependencies:
```bash
npm install
# or
yarn install
```

3. Set up environment variables:
   - Copy `.env.example` to `.env.development`:
   ```bash
   cp .env.example .env.development
   ```
   - Fill in your Firebase configuration in `.env.development`:
   ```
   REACT_APP_FIREBASE_API_KEY=your_api_key
   REACT_APP_FIREBASE_AUTH_DOMAIN=your_auth_domain
   REACT_APP_FIREBASE_PROJECT_ID=your_project_id
   REACT_APP_FIREBASE_STORAGE_BUCKET=your_storage_bucket
   REACT_APP_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
   REACT_APP_FIREBASE_APP_ID=your_app_id
   REACT_APP_FIREBASE_MEASUREMENT_ID=your_measurement_id
   ```

4. Start the development server:
```bash
npm start
# or
yarn start
```

The app will be available at [http://localhost:3000](http://localhost:3000).

## Project Structure

```
src/
├── components/          # Reusable components
│   ├── AuthProvider.js  # Authentication context provider
│   └── ProtectedRoute.js# Route protection wrapper
├── pages/              # Page components
│   ├── Home.js         # Home page (protected)
│   └── Login.js        # Login page with Google SSO
├── utils/              # Utility functions
│   └── envCheck.js     # Environment variable validation
├── firebase.js         # Firebase configuration
└── App.js             # Main application component
```

## Available Scripts

- `npm start` or `yarn start`: Run the development server
- `npm build` or `yarn build`: Build for production
- `npm test` or `yarn test`: Run tests
- `npm eject` or `yarn eject`: Eject from Create React App

## Environment Variables

The following environment variables are required:

- `REACT_APP_FIREBASE_API_KEY`: Firebase API Key
- `REACT_APP_FIREBASE_AUTH_DOMAIN`: Firebase Auth Domain
- `REACT_APP_FIREBASE_PROJECT_ID`: Firebase Project ID
- `REACT_APP_FIREBASE_STORAGE_BUCKET`: Firebase Storage Bucket
- `REACT_APP_FIREBASE_MESSAGING_SENDER_ID`: Firebase Messaging Sender ID
- `REACT_APP_FIREBASE_APP_ID`: Firebase App ID
- `REACT_APP_FIREBASE_MEASUREMENT_ID`: Firebase Measurement ID

## Authentication Flow

1. Users visit the application
2. If not authenticated, they are redirected to the login page
3. Users can sign in using their Google account
4. Upon successful authentication, users are redirected to the home page
5. Protected routes are only accessible to authenticated users

## Technologies Used

- [React](https://reactjs.org/)
- [Firebase Authentication](https://firebase.google.com/docs/auth)
- [React Router](https://reactrouter.com/)
- [Tailwind CSS](https://tailwindcss.com/)

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
