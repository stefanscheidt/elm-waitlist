# Waitlist App

Sample Application from [Elm Beyond the Basics](http://courses.knowthen.com/courses/elm-beyond-the-basics).

### Setup

Run the following setup steps

1. Run `npm install` to install the build process dependancies
2. Run `npm install gulp -g` to install the gulp executable globally
3. Run `elm package install ` to install the elm dependancies

### Setup Firebase

1. Create an account on firebase and create a new database
2. Add The following temporary rules to your firebase database

```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

Orginal values:

```json
{
  "rules": {
    ".read": "auth != null",
    ".write": "auth != null"
  }
}
```

3. Add a file the `config.js` file with your new firebase API keys, found "here"
(replace YOURFIREBASEDBHERE, then click Add Firebase to your web app)

<https://console.firebase.google.com/project/YOURFIREBASEDBHERE/settings/general/>

`config.js` should look like so:

```js
'use strict';
var config = {
  apiKey: "YOURAPIKEYHERE",
  authDomain: "YOURAUTHDOMAINHERE",
  databaseURL: "YOURURLHERE",
  storageBucket: "YOURSTORAGEBUCKER",
  messagingSenderId: "YOURMESSAGINGSENDERID"
};
```

### Start Build Process

1. Run `gulp` to start the build process
