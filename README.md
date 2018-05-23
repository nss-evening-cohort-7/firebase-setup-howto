### Firebase Setup:	
  - Go to https://firebase.google.com/
  - [One time]: Sign up for a firebase account
  - Go To Console
  - [Once per project]: Add project / Create Project
  - [Once per project]: Add Firebase to Web App
  - [Once per project]: Add CDN link to index.html (Above your dist/app.js!)
  - [Once per project]: Add Firebase config to private json (a git-ignored JSON that you can call with AJAX later) 
    ```
    {
      "firebaseKeys": {
        "apiKey": "",
        "authDomain": "",
        "databaseURL": "",
        "projectId": "",
        "storageBucket": "",
        "messagingSenderId": ""
      }
    }
    ```
  - [Once per project]: Use Ajax to load in keys from json, then pass them to firebase.initializeApp(results.firebaseKeys)
  - [Once per project]: Adjust .eslintrc.json to have an ignore on the global variable 'firebase'
    ```
      "globals": {
        "firebase": true
      },
    ```
  - [Once per project]: Set firebase rules to temporarily be defined as true.
    ```
    {
      "rules": {
        ".read": true,
        ".write": true
      }
    }
    ```
