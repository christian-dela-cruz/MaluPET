# MaluPET 🐾

**Your Pet's Best Friend** — A native Android app for managing your pets and scheduling their care appointments.

## About

MaluPET is an Android mobile application that helps pet owners keep track of their pets and manage care appointments. With MaluPET you can:

- **Register & Login** — Create an account and securely sign in.
- **Manage Pets** — Add and view your pet profiles (name, type, breed, age).
- **Schedule Appointments** — Track feeding times, grooming dates, and veterinary visits.

## Technology Stack

| Component | Technology |
|-----------|-----------|
| Language | Kotlin 2.0.21 |
| UI Framework | Jetpack Compose + Material Design 3 |
| HTTP Client | Ktor Client (CIO) |
| Build System | Gradle (Kotlin DSL) |
| Min SDK | 21+ |

## Getting Started

### Prerequisites

- Android Studio (latest stable version recommended)
- Android SDK 21+
- A running instance of the MaluPET REST API backend

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/christian-dela-cruz/MaluPET.git
   cd MaluPET
   ```

2. **Configure the backend URL**

   Open `gradle.properties` and set the `BASE_URL` property to your server's address:
   ```properties
   BASE_URL=http\://your-server-ip/MaluPET/REST
   ```

   This value is injected at build time as `BuildConfig.BASE_URL` and used in `LoginActivity.kt` and `RegisterActivity.kt`.

3. **Build and run**

   Open the project in Android Studio and run it on an emulator or a physical device, or use the command line:
   ```bash
   ./gradlew assembleDebug
   ```

## Project Structure

```
app/src/main/java/com/example/
├── it140pmp/               # Authentication & main flow (Jetpack Compose)
│   ├── MainActivity.kt     # Landing page
│   ├── LoginActivity.kt    # Login screen
│   ├── RegisterActivity.kt # Registration screen
│   └── HomePageActivity.kt # Home screen (after login)
└── malupet/                # Pet management (XML layouts)
    ├── MainActivity.kt     # Add/view pets
    ├── PetListActivity.kt  # Pet list
    ├── AppointmentActivity.kt      # Schedule appointments
    └── ViewAppointmentsActivity.kt # View all appointments
```

## License

This project is for educational purposes.
