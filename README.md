
# Catering Reservation and Ordering System

## Overview

The Catering Reservation and Ordering System is a web-based application that allows users to browse food items, add items to their cart, and place orders. Admins have the ability to create and display their products for users to purchase. The system is built using HTML, CSS, and JavaScript, and leverages Firebase for authentication and database management. The application can be run from the `main.html` file.

## Features

- **User Registration and Login**: Users can create an account and log in to place orders using Firebase Authentication.
- **Food Item Browsing**: Users can view available food items with descriptions and prices.
- **Add to Cart**: Users can add desired food items to their cart.
- **Order Placement**: Users can place orders for the items in their cart.
- **Admin Panel**: Admins can create and manage food items for display on the site using Firebase Firestore.
- **Responsive Design**: The application is responsive and works well on both desktop and mobile devices.

## Technologies Used

- **HTML**: Markup language for structuring the web pages.
- **CSS**: Styling the web pages to make them visually appealing.
- **JavaScript**: Adding interactivity and functionality to the web pages.
- **Firebase**: Backend-as-a-Service for authentication and database management.

## File Structure

```
/catering-system
│
├── css
│   ├── styles.css
│
├── js
│   ├── main.js
│   ├── admin.js
│   ├── user.js
│   ├── firebase-config.js
│
├── index.html
├── main.html
├── login.html
├── register.html
├── admin.html
├── cart.html
├── order.html
│
└── README.md
```

## Setup

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/yourusername/catering-system.git
   ```

2. **Navigate to the Project Directory**:
   ```sh
   cd catering-system
   ```

3. **Set Up Firebase**:
   - Go to [Firebase Console](https://console.firebase.google.com/).
   - Create a new project.
   - Add a web app to your project.
   - Copy the Firebase SDK configuration and initialize Firebase in `firebase-config.js`.

4. **Initialize Firebase in `firebase-config.js`**:
   ```javascript
   // Import the functions you need from the SDKs you need
   import { initializeApp } from "https://www.gstatic.com/firebasejs/9.0.0/firebase-app.js";
   import { getAuth } from "https://www.gstatic.com/firebasejs/9.0.0/firebase-auth.js";
   import { getFirestore } from "https://www.gstatic.com/firebasejs/9.0.0/firebase-firestore.js";

   // Your web app's Firebase configuration
   const firebaseConfig = {
     apiKey: "YOUR_API_KEY",
     authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
     projectId: "YOUR_PROJECT_ID",
     storageBucket: "YOUR_PROJECT_ID.appspot.com",
     messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
     appId: "YOUR_APP_ID"
   };

   // Initialize Firebase
   const app = initializeApp(firebaseConfig);
   const auth = getAuth(app);
   const db = getFirestore(app);
   ```

5. **Open `main.html` in Your Browser**:
   You can open the `main.html` file directly in your browser to start using the application.

## Usage

1. **User Registration**:
   - Open `register.html` to create a new account using Firebase Authentication.

2. **User Login**:
   - Open `login.html` to log into your account using Firebase Authentication.

3. **Browse Food Items**:
   - After logging in, you can view food items on `main.html`, which are fetched from Firebase Firestore.

4. **Add Items to Cart**:
   - Click on the "Add to Cart" button next to the desired food items.

5. **View Cart and Place Order**:
   - Go to `cart.html` to view items in your cart and proceed to place an order, storing the order details in Firebase Firestore.

6. **Admin Operations**:
   - Admins can log in through `admin.html` to add or manage food items in Firebase Firestore.
