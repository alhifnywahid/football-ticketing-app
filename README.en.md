<b>English</b> | <a href="./README.md">Indonesia</a>

---

![icon](./file/icon_new.png)

![Thumbnail](./file/thumbnail.png)

# Bolatix - Football Ticket Booking Application

Bolatix is an Android application for digitally booking football match tickets. Built as a team project in the Bangkit Academy Independent Study program, it combines mobile technology, cloud services, and artificial intelligence to deliver a seamless, fast, and secure ticket booking experience.

## Table of Contents

- [About the Project](#about-the-project)
- [Features](#features)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Screenshots](#screenshots)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Downloads](#downloads)
- [Team](#team)
- [License](#license)

---

## About the Project

Bolatix was built to address the need for Indonesian football fans to access match tickets digitally. With machine learning-powered recommendations, users can discover relevant matches based on their favorite teams or past purchase history. Payments are integrated with Midtrans, supporting a wide range of common Indonesian payment methods. Tickets are generated as downloadable PDF files that can be shared directly from the app.

This project is the result of collaboration across three specializations: Mobile Development, Cloud Computing, and Machine Learning within the Bangkit Academy ecosystem.

---

## Features

| Feature | Description |
|---|---|
| Authentication | Register and sign in using email/password and Google Sign-In |
| Onboarding | Introductory walkthrough for new users |
| Home Screen | Displays upcoming matches and personalized recommendations |
| Smart Recommendations | Match recommendations based on favorite teams and purchase history (ML) |
| Ticket Booking | Select match, tribune class, and entry gate |
| Payment Gateway | Integrated Midtrans payments (multi-method support) |
| Payment Verification | Data review and confirmation before finalizing a transaction |
| Order History | Full list of past ticket transactions |
| PDF Ticket | Download and share tickets as PDF files |
| Standings | View current league standings |
| Favorite Team | Select and save favorite teams for more accurate recommendations |
| User Profile | Update profile picture, name, and personal information |
| Notifications | In-app notifications for transactions and match information |
| Forgot Password | Password reset via email |
| FAQ | Frequently asked questions |
| Privacy Policy | Privacy policy and terms of use |
| About Us | Information about the team and application |

---

## Architecture

The application implements the **MVVM (Model-View-ViewModel)** architectural pattern with a lightweight Clean Architecture approach, organized into three main layers:

```
app/src/main/java/com/example/bolatix/
├── data/
│   ├── firebase/        # Firebase Auth, Firestore, and FCM helpers
│   ├── models/          # Data classes (User, Team, Stadium, Gate, etc.)
│   ├── remote/
│   │   ├── network/     # Retrofit service interface and interceptors
│   │   └── response/    # API response data classes
│   └── repository/      # AuthRepository and FootballRepository
├── di/                  # Koin dependency injection module
├── preference/          # DataStore for onboarding and user preferences
├── ui/
│   ├── activities/      # All Activities (18 activities)
│   ├── adapters/        # RecyclerView Adapters
│   ├── components/      # Custom UI components
│   ├── fragments/       # Fragments (Home, Standings, Orders, Profile)
│   └── viewmodels/      # ViewModels for each feature
└── utils/               # Utility and extension functions
```

---

## Tech Stack

### Mobile (Android)
| Library | Version | Purpose |
|---|---|---|
| Kotlin | - | Primary programming language |
| Android SDK | min 24 / target 34 | Android platform |
| ViewBinding | - | Type-safe layout binding |
| Navigation Component | - | Fragment navigation |
| Firebase Authentication | - | Email and Google authentication |
| Firebase Firestore | - | User data and notifications database |
| Retrofit 2 | - | HTTP communication to REST API |
| OkHttp Logging Interceptor | - | Request logging and retry |
| Koin | - | Dependency Injection |
| Glide | - | Image loading from URL |
| UCrop | - | Profile image cropping |
| Midtrans SDK (UIKit) | - | Payment gateway |
| Progress Button | - | Button with loading animation |
| ViewPager2 | - | Onboarding slides |
| DataStore Preferences | - | Local preference storage |
| Markwon Core | - | Markdown content rendering |
| Material 3 | - | Material Design 3 UI components |

### Backend
- REST API hosted on Cloud Run (Google Cloud Platform)
- Base URL: `https://bolatix-552077162382.asia-southeast2.run.app/api/`
- Backend Repository: [BolaTix/Cloud-Computing](https://github.com/BolaTix/Cloud-Computing)

### Machine Learning
- Recommendation model based on purchase history and team preferences
- ML Repository: [BolaTix/Machine-Learning](https://github.com/BolaTix/Machine-Learning)

---

## Screenshots

<details>
  <summary>View screenshots</summary>
  <table>
    <tr>
      <td><img src="./file/screenshoot/1.png" alt="1" width="100%"></td>
      <td><img src="./file/screenshoot/2.png" alt="2" width="100%"></td>
      <td><img src="./file/screenshoot/3.png" alt="3" width="100%"></td>
      <td><img src="./file/screenshoot/4.png" alt="4" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/5.png" alt="5" width="100%"></td>
      <td><img src="./file/screenshoot/6.png" alt="6" width="100%"></td>
      <td><img src="./file/screenshoot/7.png" alt="7" width="100%"></td>
      <td><img src="./file/screenshoot/8.png" alt="8" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/9.png" alt="9" width="100%"></td>
      <td><img src="./file/screenshoot/10.png" alt="10" width="100%"></td>
      <td><img src="./file/screenshoot/11.png" alt="11" width="100%"></td>
      <td><img src="./file/screenshoot/12.png" alt="12" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/13.png" alt="13" width="100%"></td>
      <td><img src="./file/screenshoot/14.png" alt="14" width="100%"></td>
      <td><img src="./file/screenshoot/15.png" alt="15" width="100%"></td>
      <td><img src="./file/screenshoot/16.png" alt="16" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/17.png" alt="17" width="100%"></td>
      <td><img src="./file/screenshoot/18.png" alt="18" width="100%"></td>
      <td><img src="./file/screenshoot/19.png" alt="19" width="100%"></td>
      <td><img src="./file/screenshoot/20.png" alt="20" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/21.png" alt="21" width="100%"></td>
      <td><img src="./file/screenshoot/22.png" alt="22" width="100%"></td>
      <td><img src="./file/screenshoot/23.png" alt="23" width="100%"></td>
      <td><img src="./file/screenshoot/24.png" alt="24" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/25.png" alt="25" width="100%"></td>
      <td><img src="./file/screenshoot/26.png" alt="26" width="100%"></td>
      <td><img src="./file/screenshoot/27.png" alt="27" width="100%"></td>
      <td><img src="./file/screenshoot/28.png" alt="28" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/29.png" alt="29" width="100%"></td>
      <td><img src="./file/screenshoot/30.png" alt="30" width="100%"></td>
      <td><img src="./file/screenshoot/31.png" alt="31" width="100%"></td>
      <td><img src="./file/screenshoot/32.png" alt="32" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/33.png" alt="33" width="100%"></td>
      <td><img src="./file/screenshoot/34.png" alt="34" width="100%"></td>
      <td><img src="./file/screenshoot/35.png" alt="35" width="100%"></td>
      <td><img src="./file/screenshoot/36.png" alt="36" width="100%"></td>
    </tr>
    <tr>
      <td><img src="./file/screenshoot/37.png" alt="37" width="100%"></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </table>
</details>

---

## Prerequisites

Before running this project, make sure you have the following ready:

- Android Studio Hedgehog or later
- JDK 8 or later
- Android SDK with minimum API Level 24
- A Firebase project (for `google-services.json` configuration)
- A Midtrans Sandbox account (for client key configuration)
- An active internet connection

---

## Installation

1. **Clone the repository**

```bash
git clone https://github.com/BolaTix/Mobile-Development.git
cd Mobile-Development
```

2. **Configure Firebase**

   - Create a project in the [Firebase Console](https://console.firebase.google.com/)
   - Enable Firebase Authentication (Email/Password and Google Sign-In)
   - Enable Cloud Firestore
   - Download `google-services.json` and place it in the `app/` directory

3. **Configure Midtrans**

   Open `app/build.gradle.kts` and update the following values:

   ```kotlin
   buildConfigField("String", "MERCHANT_KEY", "\"<your-sandbox-client-key>\"")
   buildConfigField("String", "MIDTRANS_URL_CHARGE", "\"<your-charge-server-url>\"")
   ```

4. **Open in Android Studio**

   - Open Android Studio, select `File > Open`, and navigate to the project folder
   - Wait for the Gradle sync to complete

5. **Run the Application**

   - Connect an Android device (API 24+) or use an emulator
   - Press the `Run` button in Android Studio

---

## Downloads

| Resource | Link |
|---|---|
| Android Application (APK) | [Download BOLATIX.apk](./file/BOLATIX.apk) |
| Figma Design File | [Download FGMA-BOLATIX.fig](./file/FGMA-BOLATIX.fig) |
| Backend Repository | [BolaTix/Cloud-Computing](https://github.com/BolaTix/Cloud-Computing) |
| Machine Learning Repository | [BolaTix/Machine-Learning](https://github.com/BolaTix/Machine-Learning) |

---

## Team

This project was developed by the Mobile Development team in the **Bangkit Academy** Independent Study (Studi Independen Bersertifikat) program.

---

## License

This project is licensed under the **MIT License**. See the [LICENSE](./LICENSE) file for full details.
