# 🔥 Flutter Firebase Authentication + Firestore

Create a new project on Firebase Console

Enable Email/Password Authentication in Firebase → Authentication → Sign-in method.

Create a Firestore database (start in Test Mode for development).

⚡ Flutter Setup

Install Firebase packages in pubspec.yaml:

firebase_core
firebase_auth
cloud_firestore


Run:

flutter pub get
flutterfire configure


→ This generates firebase_options.dart.

👨‍💻 Implementation Steps

Initialize Firebase in main.dart:

await Firebase.initializeApp(options: DefaultFirebaseOptions.currentPlatform);


Create Login Screen:

signInWithEmailAndPassword(email, password)

Redirect to Home if login success.

Create Signup Screen:

createUserWithEmailAndPassword(email, password)

Save user details (name, email) to Firestore → users collection.

Create Home Screen:

Fetch user document from Firestore (users/{uid})

Show name + email

Add Logout button → FirebaseAuth.instance.signOut()


# 🔥 Flutter Firebase Authentication + Firestore

A Flutter app with Firebase **Email/Password Authentication** and **Firestore database integration**.

## 🚀 Features
- User Signup (store name + email in Firestore)
- User Login
- Profile/Home Screen with Firestore data
- Logout functionality

## 📦 Packages Used
- firebase_core
- firebase_auth
- cloud_firestore
- cupertino_icons

## 🛠 Setup
1. Clone repo  
2. Run `flutter pub get`  
3. Configure Firebase: `flutterfire configure`  
4. Add `google-services.json` (Android) or `GoogleService-Info.plist` (iOS)  
5. Run app 🚀  

## 📂 Screens
- **Login Screen** → Login with email/password  
- **Signup Screen** → Create account & save to Firestore  
- **Home Screen** → Show user profile + logout  
