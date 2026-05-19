🚖 Ride Booking App (Swift Ride)

A full-featured ride booking mobile application built with Flutter, integrated with Firebase, Google Maps API, and Gemini AI for smart assistant features.

📱 Features
👤 User System
User Signup & Login (Firebase Authentication)
Passenger & Rider role selection
Profile management
🚗 Ride System
Book a ride instantly
Live ride tracking
Ride history
Ride requests (for riders)
🗺️ Google Maps Integration
Real-time location tracking
Pickup & destination selection
Map-based route visualization
Address auto-complete & location picker
🤖 Gemini AI Integration
AI Chat Assistant inside app
Ride-related help (fare, routes, issues)
Smart suggestions for users
Support assistant for passengers & riders
💳 Payments & Earnings
Ride fare calculation
Rider earnings dashboard
🔔 Notifications
Ride status updates
Request alerts
🧠 Tech Stack
Flutter (Frontend)
Dart
Firebase
Authentication
Firestore Database
Cloud Messaging (optional)
Google Maps API
Gemini AI API
Node.js / Flask Backend (if used for ML or APIs)
🧩 Project Structure
lib/
│── main.dart
│
├── screens/
│   ├── login_screen.dart
│   ├── signup_screen.dart
│   ├── splash_screen.dart
│   ├── user_selection_screen.dart
│   ├── passenger_home_screen.dart
│   ├── rider_home_screen.dart
│   ├── booking_screen.dart
│   ├── live_tracking_screen.dart
│   ├── gemini_chat_screen.dart
│   ├── map_picker_screen.dart
│   └── ...
│
├── widgets/
│   ├── passenger_drawer.dart
│   └── rider_drawer.dart
│
├── services/
│   ├── firebase_service.dart
│   ├── location_service.dart
│   ├── gemini_service.dart
│   └── map_service.dart
🔑 API Setup
1️⃣ Firebase Setup
Add google-services.json in:
android/app/
Add Firebase configuration in:
lib/firebase_options.dart
2️⃣ Google Maps API Setup

Enable in Google Cloud Console:

Maps SDK for Android
Maps SDK for iOS
Places API

Add API key in:

Android
android/app/src/main/AndroidManifest.xml
<meta-data
    android:name="com.google.android.geo.API_KEY"
    android:value="YOUR_GOOGLE_MAPS_API_KEY"/>
iOS
ios/Runner/AppDelegate.swift
3️⃣ Gemini AI Setup

Used for AI chat assistant inside the app.

Add API key in .env or config file:

GEMINI_API_KEY=your_api_key_here

Example usage (Dart):

final response = await GeminiService.sendMessage(
  message: "Find cheapest ride near me",
);
🤖 Gemini AI Features
Ride suggestions
Fare estimation help
User support chatbot
Smart route recommendations
Error/help assistant
🗺️ Google Maps Features
Current location detection
Pickup & drop selection
Route drawing between points
Distance & time estimation
Live tracking (driver movement)
🚀 How to Run Project
1. Clone Repo
git clone https://github.com/your-username/swift-ride.git
cd swift-ride
2. Install dependencies
flutter pub get
3. Run app
flutter run
🧪 Testing
Run on emulator or real device
Ensure:
Internet enabled
Location permission granted
Firebase connected
📦 Build APK
flutter build apk --release

APK location:

build/app/outputs/flutter-apk/app-release.apk
⚠️ Known Issues
Location permission required for maps
Firebase setup must be correct
API keys must be enabled in Google Cloud Console
👨‍💻 Developer Notes

This project is designed as a real-world ride booking system similar to Uber/Ola with added AI capabilities using Gemini API.

Future improvements:

Dynamic pricing model
Driver navigation mode
Multi-city support
AI route optimization
📄 License

This project is for educational and portfolio use.
