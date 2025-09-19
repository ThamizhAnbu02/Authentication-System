Firebase Authentication Web App
This is a web application that implements user authentication using Firebase Authentication and Firestore. It includes user sign-up, sign-in, and a basic homepage displaying user information.
Features

User Sign-Up: Allows users to create an account with their first name, last name, email, and password.
User Sign-In: Allows users to log in with their email and password.
Firestore Integration: Stores user data (email, first name, last name) in Firestore upon sign-up.
Responsive UI: Includes a clean and modern user interface with CSS animations and transitions.
Homepage: Displays the logged-in user's information after successful sign-in.

Prerequisites

A modern web browser (Chrome, Firefox, Edge, etc.).
A Firebase project with Authentication (Email/Password) and Firestore enabled.
Basic knowledge of HTML, CSS, and JavaScript.

Setup Instructions

Clone the Repository
git clone <repository-url>
cd <repository-folder>


Set Up Firebase

Create a Firebase project at Firebase Console.
Enable Email/Password authentication in the Authentication section.
Enable Firestore in the Firestore Database section.
Copy your Firebase project configuration and replace the firebaseConfig object in firebaseauth.js with your own configuration:const firebaseConfig = {
  apiKey: "your-api-key",
  authDomain: "your-auth-domain",
  projectId: "your-project-id",
  storageBucket: "your-storage-bucket",
  messagingSenderId: "your-messaging-sender-id",
  appId: "your-app-id",
  measurementId: "your-measurement-id"
};




Serve the Application

You can use a local server to run the application. For example, using Python:python -m http.server 8000


Open your browser and navigate to http://localhost:8000.


File Structure
├── index.html         # Main page with sign-up and sign-in forms
├── homepage.html      # Homepage displayed after successful login
├── style.css         # Styles for the application
├── script.js         # Handles form toggling between sign-up and sign-in
├── firebaseauth.js   # Firebase authentication and Firestore logic
└── README.md         # This file



Usage

Sign Up: Enter your first name, last name, email, and password in the sign-up form and click "Sign Up". The user data will be stored in Firestore, and you will be redirected to the homepage.
Sign In: Enter your email and password in the sign-in form and click "Sign In". Upon successful login, you will be redirected to the homepage.
Homepage: Displays the logged-in user's first name, last name, and email. A logout button is available (though logout functionality is not implemented in the provided code).
Form Toggling: Click "Sign Up" or "Sign In" links to switch between the sign-up and sign-in forms.

Notes

The Firebase configuration in firebaseauth.js uses placeholder values. Replace them with your actual Firebase project configuration to avoid errors.
The logout functionality is not implemented in the provided code. To add it, you can use Firebase's signOut method and redirect the user to index.html.
Ensure your Firebase security rules for Authentication and Firestore are properly configured to allow read/write operations.

Dependencies

Firebase SDK (v10.11.1) for Authentication and Firestore, loaded via CDN.
Font Awesome for icons (used in the UI).
Poppins font (used in style.css).

Contributing

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes and commit (git commit -m 'Add some feature').
Push to the branch (git push origin feature-branch).
Create a Pull Request.

License
This project is licensed under the MIT License.
