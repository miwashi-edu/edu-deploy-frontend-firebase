# edu-deploy-frontend-firebase


## Skapa firebase project

## bash

```bash
curl -sL https://firebase.tools | bash

mkdir frontend-app
cd frontend-app
npx create-react-app .

npm install firebase
vi ./src/firebase.js

firebase login
```

## firebase.js

```bash
import firebase from 'firebase/app';
import 'firebase/analytics'; // Only if you want to use Firebase Analytics

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID",
  measurementId: "YOUR_MEASUREMENT_ID" // Only if you want to use Firebase Analytics
};

// Initialize Firebase
firebase.initializeApp(firebaseConfig);
```

