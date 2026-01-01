# SoulSync - Personalized Mood Tracker

A web application for tracking moods and receiving personalized activity suggestions.

## Features

- User authentication (Login/Sign Up)
- Mood tracking dashboard
- Personalized activity, article, strategy, and music suggestions
- Mood history with add, edit, and delete functionality
- Beautiful teal-themed UI

## Setup

1. Install dependencies:
```bash
npm install
```

2. Configure Firebase:
   - Create a Firebase project at https://console.firebase.google.com
   - Enable Authentication (Email/Password)
   - Create a Firestore database
   - Copy your Firebase config to `src/firebase/config.js`

3. Run the development server:
```bash
npm run dev
```

## Firebase Configuration

Create `src/firebase/config.js` with your Firebase credentials:

```javascript
import { initializeApp } from 'firebase/app';
import { getAuth } from 'firebase/auth';
import { getFirestore } from 'firebase/firestore';

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};

const app = initializeApp(firebaseConfig);
export const auth = getAuth(app);
export const db = getFirestore(app);
```

