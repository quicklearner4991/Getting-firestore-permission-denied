### Getting 'firestore/permission-denied' while integrating firestore in React native mobile app

# To solve this error 

Go to firebase console and move to firestore setting and change the setting like this.

```service cloud.firestore {
  match /databases/{database}/documents {
    match /todos/{document=**} {
      allow read, write: if true;
    }
  }
```}


