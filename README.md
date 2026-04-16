


# BarberQueue ✂️

🚀 **Live App:** https://barberqueue-sys.web.app

**BarberQueue** is a modern, real-time smart queue management system designed to streamline barbershop operations. It eliminates long physical waiting times by allowing customers to discover nearby shops, join virtual queues, and get accurate ETAs before they even arrive. Shop owners benefit from an intuitive dashboard to manage services, track customers, and optimize their daily workflow.

---

## 🌟 Key Features

### For Customers (Users)
- **Find a Barbershop**: Search for shops by name or filter by city via a responsive interface.
- **Real-Time Queueing**: Select desired services and join a queue instantly with just a phone number and name.
- **Status & ETA Tracking**: Check your queue status and Estimated Time of Arrival (ETA) dynamically based on the shop's active services.
- **Flexible Management**: Easily exit the queue if plans change.

### For Barbershop Owners
- **Easy Onboarding**: Secure login and quick initial shop configuration (name, location, business hours).
- **Service Management**: Add or remove shop services along with their specific time durations.
- **Queue Dashboard**: View the active queue, monitor customer ETAs, and mark customers as "Served" with a single click.
- **Queue Controls**: Toggle the "Accepting Customers" status on or off to manage heavy traffic.

### Core Architecture
- **Automatic Theme Toggling**: Built-in Dark/Light mode support respecting system preferences.
- **Responsive UI**: Fully responsive, mobile-first design powered by Tailwind CSS.

---

## 🛠️ Technology Stack

- **Frontend Core**: HTML5, Vanilla JavaScript (ESM modules), CSS3.
- **Styling**: Tailwind CSS (loaded via CDN) & custom Glassmorphism aesthetics.
- **Backend/Database**: 
  - **Firebase Firestore**: Real-time NoSQL database for queue and shop state tracking.
  - **Firebase Authentication**: Secure owner registration and login handling.
  - **Firebase Hosting**: Native configuration for easy web deployment.

---

## 🚀 Installation & Setup

Want to run BarberQueue locally or contribute? Follow these steps!

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/BarberQueue.git
cd BarberQueue
```

### 2. Configure Firebase Credentials
Because security is a priority, Firebase credentials are not hardcoded into the project files.
1. Navigate to the `public/` directory.
2. You will find a file named `firebase-config.example.js`.
3. Copy or rename this file to `firebase-config.js`:
   ```bash
   cp public/firebase-config.example.js public/firebase-config.js
   ```
4. Open `public/firebase-config.js` and replace the placeholder keys with your actual Firebase project credentials:
   ```javascript
   export const firebaseConfig = {
     apiKey: "YOUR_API_KEY",
     authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
     projectId: "YOUR_PROJECT_ID",
     storageBucket: "YOUR_PROJECT_ID.firebasestorage.app",
     messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
     appId: "YOUR_APP_ID",
     measurementId: "YOUR_MEASUREMENT_ID"
   };
   ```

### 3. Run the Application
Since the project relies entirely on static assets and Firebase, you only need to serve the `public/` folder. You can use standard local HTTP servers:

Using `npx` (Node.js):
```bash
npx serve public -p 3000
```
Then, open `http://localhost:3000` in your browser.

---

## 📂 Project Structure

```text
BarberQueue/
├── public/                 # Main application code (Served to users)
│   ├── index.html          # Landing page
│   ├── search.html         # Customer search and queue joining interface
│   ├── auth.html           # Owner authentication (Login/Registration)
│   ├── setup.html          # Owner initial shop configuration step
│   ├── owner.html          # Owner dashboard for queue management
│   ├── firebase-config.js          # (Ignored) Active Firebase credentials
│   └── firebase-config.example.js  # Template for Firebase credentials
├── firebase.json           # Firebase hosting deployment configuration
├── firestore.rules         # Firebase Firestore security rules
├── firestore.indexes.json  # Firebase Firestore index definitions
├── .gitignore              # Ignored files, environments, and cache
└── README.md               # Project documentation
```

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! 
Feel free to check out the [issues page](../../issues).

## 📄 License
This project is licensed under the MIT License. Built with ❤️ for modern barbershops.
