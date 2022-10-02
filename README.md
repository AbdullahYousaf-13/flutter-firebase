# Flutter & Firebase:

- In this Flutter & Firebase tutorial series, we'll build a complete app with a database (Firebase Firestore) and an authentication system (using Firebase auth)

- - -

## What is Firebase:

- A service made by Google 

- Offers lots of different things like cloud hosting, storage, authentication services and a real time databases called fire store

- - -

## Why Use Firebase:

- Acts as a back end to our apps so we can focus on flutter instead of worring about all the authentication and data base stuf on the back end fire base can take care of alot of that for us and makes it realy simple to implement inside our flutter apps

- To link firebase to our flutter as a back end

- - -

## Creating and Setting up a firebase project:

- Go to firebase web 

- Click on 'console'

- Click on 'Add project'

- Enter The name of your project and click on 'continue'

- Uncheck 'Enable Google Analytics for the project' and click on 'Create project'

- Once done click on 'continue'

- Click on andriod icon to set up a new app for this back end

- Go to vs code andriod/app folder and open file 'build.gradle' go to the 'defaultConfig' section and copy the applicationId like `com.`[desired-name]`.brew_crew` and paste it inside 'Andriod package name' field and give it a nickname inside 'App nickname' field then click on 'register app'

- Click on 'Download google-service.json' click on 'show in folder' copy it and paste it inside the 'app' folder in our project

- Click on 'Next' copy classpath like this `classpath 'com.google.gms:google-services:4.3.13'`  Go to vs code andriod folder and open file 'build.gradle' go to the 'dependencies' section and paste it

- Copy second plugin id like this `id 'com.google.gms.google-services'` Go to vs code andriod/app folder and open file 'build.gradle' go to the bottom and paste it

- To add a package go to web 'pub.dev' search your desired package copy its dependencies from the tab 'installing' like this `firebase_auth: ^3.11.0`, `cloud_firestore: ^3.5.0`, go to your editor, open file 'pubspec.yaml' go to 'dependencies' section under `cupertino_icons: ^1.0.2` paste the dependencies there with one tab then go to your file and click on 'Get dependencies'

- - -

## My Dart Codes with Explanations:

### Basic App Structure:

#### Code:

##### main.dart:

    import 'package:brew_crew/screens/wrapper.dart';
    import 'package:flutter/material.dart';

    void main() {
      runApp(const MyApp());
    }

    class MyApp extends StatelessWidget {
      const MyApp({Key? key}) : super(key: key);

      // This widget is the root of your application.
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          home: Wrapper(),
        );
      }
    }

##### wrapper.dart

    import 'package:brew_crew/screens/authenticate/authenticate.dart';
    import 'package:brew_crew/screens/home/home.dart';
    import 'package:flutter/material.dart';

    class Wrapper extends StatelessWidget {
      const Wrapper({Key? key}) : super(key: key);

      @override
      Widget build(BuildContext context) {
        //return either Home or Authenticate widget
        return Authenticate();
      }
    }

##### authenticate.dart:

    import 'package:flutter/material.dart';

    class Authenticate extends StatefulWidget {
      const Authenticate({Key? key}) : super(key: key);

      @override
      State<Authenticate> createState() => _AuthenticateState();
    }

    class _AuthenticateState extends State<Authenticate> {
      @override
      Widget build(BuildContext context) {
        return Container(
          child: Text('Authenticate'),
        );
      }
    }

##### home.dart:

    import 'package:flutter/material.dart';

    class Home extends StatelessWidget {
      const Home({Key? key}) : super(key: key);

      @override
      Widget build(BuildContext context) {
        return Container(
          child: Text('Home'),
        );
      }
    }

#### Explanation:

##### main.dart:

- main function which runs when the flutter app first start fires function 'runnApp(MyApp());' which registers 'MyApp()' as our root widget which is currently 'MaterialApp' widget

- Inside 'MaterialApp' widget we will write 'home wrapper(),' which is saying that the 'Wrapper' should be the home screen like this:

      import 'package:brew_crew/screens/wrapper.dart';
      import 'package:flutter/material.dart';

      void main() {
        runApp(const MyApp());
      }

      class MyApp extends StatelessWidget {
        const MyApp({Key? key}) : super(key: key);

        // This widget is the root of your application.
        @override
        Widget build(BuildContext context) {
          return MaterialApp(
            home: Wrapper(),
          );
        }
      }

##### wrapper.dart:

- 'wrapper.dart': anchor of the whole app, listen for auth changes (logged in or not) the widget thats going to wrapp the 'Authenticate' widget or the 'Home' widget

- `import 'package:flutter/material.dart';`(importing material so we can use 'material.dart' package)

- Creating a 'stateless' widget by writing 'stles' and pressing tab and renaming it to 'Wrapper' then returning 'Home' or 'Wrapper' and press tab so it will automatically import it for you like this:

      class Wrapper extends StatelessWidget {
        const Wrapper({Key? key}) : super(key: key);

        @override
        Widget build(BuildContext context) {
          //return either Home or Authenticate widget
          return Authenticate();
        }
      }

##### authenticate.dart:

- 'authencate.dart': the widget thats going to wrapp the 'SignIn' widget or the 'Register' widget

- `import 'package:flutter/material.dart';`(importing material so we can use 'material.dart' package)

- Creating a 'statefull' widget by writing 'stful' and pressing tab and renaming it to 'Authenticate' then returning container and inside it a 'child' and then a text widget like this:

      class Authenticate extends StatefulWidget {
        const Authenticate({Key? key}) : super(key: key);

        @override
        State<Authenticate> createState() => _AuthenticateState();
      }

      class _AuthenticateState extends State<Authenticate> {
        @override
        Widget build(BuildContext context) {
          return Container(
            child: Text('Authenticate'),
          );
        }
      }

##### home.dart:

- 'home.dart': the widget thats going to wrapp the 'BrewList' widget or the 'Settings' widget

- `import 'package:flutter/material.dart';`(importing material so we can use 'material.dart' package)

- Creating a 'stateless' widget by writing 'stles' and pressing tab and renaming it to 'Home' then returning container and inside it a 'child' and then a text widget like this:

      class Home extends StatelessWidget {
        const Home({Key? key}) : super(key: key);

        @override
        Widget build(BuildContext context) {
          return Container(
            child: Text('Home'),
          );
        }
      }

- - -



- - -
- - -

#

### :

#### Code:

##### main.dart:



##### wrapper.dart:



##### home.dart:



##### authenticate.dart:



#### Explanation:

##### main.dart:



##### wrapper.dart:



##### home.dart:



##### authenticate.dart:



- - -

- - -
- - -

# Frequently used Git Commands:

- E:

- cd Programming\Flutter\flutter-with-firebase\brew_crew


- git add .

- git commit -m "Done till "

- git push origin master


- git status

---
---