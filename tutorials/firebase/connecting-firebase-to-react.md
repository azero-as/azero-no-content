# Connecting Firebase to React

Setting up a React project with Firebase is very simple. Go to https://firebase.google.com/ and login, create a project and you are already half way there.

Now run over to you React project and install firebase as an dependency by running the command:  

    npm install --save firebase

The next step is to import firebase into your project. Substitute the information in the `config` with the information you get from firebase, which is usually obtained by clicking on the web app button(usually found on the project front-page or in the project settings):

![Firebase web app info](resources/add-to-webapp.png)

You can do it directly in your code like this:

```javascript  
    import firebase from 'firebase'

    var config = {
    apiKey: "EXAMPLE123123AJSHDOAPIHOUFLNKASDHHVJAKJSKND",
    authDomain: "example.firebaseapp.com",
    databaseURL: "https://example.firebaseio.com",
    storageBucket: "example.appspot.com",
    messagingSenderId: "7654325678976543245"
    };

    var firebaseApp = firebase.initializeApp(config);

    class App extends Component {...}
```

or export it as a component that can be imported somewhere else like this:

```javascript  
    import firebase from 'firebase'

    var config = {
    apiKey: "EXAMPLE123123AJSHDOAPIHOUFLNKASDHHVJAKJSKND",
    authDomain: "example.firebaseapp.com",
    databaseURL: "https://example.firebaseio.com",
    storageBucket: "example.appspot.com",
    messagingSenderId: "7654325678976543245"
    };

    var firebaseApp = firebase.initializeApp(config);

    export default firebaseApp;
```

Now you are all set to start using Firebase for your web application. The next steps will be to query the database, set up rules and authentication.

**NOTE: If the `initializeApp` function gets triggered several times it might cause errors with duplicate connections. One possible solution is to create a `singleton` method, or do a basic `if` statement to see if it has already been initialized. An example of this can be seen below.**

    if (!firebase.apps.length) {
       firebaseApp = firebase.initializeApp(config);
    }
