# edu-deploy-frontend-firebase


## Prerequisit

> Log in on firebase and create a new project

```shell
npm install -g firebase-tools
#eller
curl -sL https://firebase.tools | bash

firebase login
```
## Instructions


```bash
cd ~
cd ws
mkdir gomoku-frontend
cd gomoku-frontend
npx create-react-app .
npm start
```

```bash
firebase init hosting
? Please select an option: Use an existing project
? Select a default Firebase project for this directory: [PROJECT] ([PROJECT])
? What do you want to use as your public directory? build
? Configure as a single-page app (rewrite all urls to /index.html)? No
? Set up automatic builds and deploys with GitHub? No
? File public/index.html already exists. Overwrite? No

npm run build
firebase deploy --only hosting
```


## edit firebase.js if needed

```bash
vi ./src/firebase.js
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

