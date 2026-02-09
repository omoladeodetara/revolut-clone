# Revolut Clone - Fintech App

A React Native fintech application built with Expo, inspired by Revolut. This app demonstrates modern mobile banking UI/UX with features like crypto trading, transfers, and lifestyle management.

## Features

- 🎨 Beautiful UI inspired by Revolut
- 🔐 Clerk authentication integration
- 💰 Crypto trading interface
- 💸 Money transfers
- 🏠 Home dashboard
- 🎯 Lifestyle and investment tracking
- 📱 Dynamic app icons
- 🔒 Biometric authentication support

## Tech Stack

- **Framework**: React Native with Expo (~50.0.14)
- **Navigation**: Expo Router (~3.4.8)
- **Authentication**: Clerk Expo (~0.20.11)
- **State Management**: Zustand (^4.5.2)
- **Data Fetching**: TanStack React Query (^5.28.9)
- **Animations**: React Native Reanimated (~3.6.2)
- **Charts**: Victory Native (^40.1.0)
- **Language**: TypeScript (^5.1.3)

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Expo CLI
- (Optional) Clerk account for authentication features

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/omoladeodetara/revolut-clone.git
   cd revolut-clone
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory:
   ```bash
   cp .env.example .env
   ```
   
   If you have a Clerk account, add your publishable key:
   ```
   EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_your_key_here
   ```
   
   **Note**: The app includes a demo mode that works without Clerk authentication. If you don't provide a valid Clerk key, you can still view the landing page.

## Running the App

### Web (Development)
```bash
npm run web
# or
npx expo start --web
```

### iOS
```bash
npm run ios
# or
npx expo run:ios
```

### Android
```bash
npm run android
# or
npx expo run:android
```

### Standard Expo Dev Server
```bash
npm start
# or
npx expo start
```

## Screenshots

### Landing Page
![Landing Page](https://github.com/user-attachments/assets/a0760c38-5d9d-475c-91d3-8d658ce51d4b)

The app features a clean, modern landing page with options to log in or sign up.

## Project Structure

```
revolut-clone/
├── app/                          # App screens and routes (Expo Router)
│   ├── (authenticated)/          # Protected routes
│   │   ├── (tabs)/              # Tab navigation
│   │   │   ├── home.tsx         # Home dashboard
│   │   │   ├── crypto.tsx       # Crypto trading
│   │   │   ├── invest.tsx       # Investment tracking
│   │   │   ├── transfers.tsx    # Money transfers
│   │   │   └── lifestyle.tsx    # Lifestyle features
│   │   ├── (modals)/            # Modal screens
│   │   │   ├── account.tsx      # Account settings
│   │   │   └── lock.tsx         # Lock screen
│   │   └── crypto/[id].tsx      # Individual crypto details
│   ├── api/                      # API routes
│   ├── verify/                   # Phone verification
│   ├── index.tsx                 # Landing page
│   ├── login.tsx                 # Login screen
│   ├── signup.tsx                # Signup screen
│   └── _layout.tsx               # Root layout
├── assets/                       # Static assets
│   ├── images/                   # App icons and images
│   └── videos/                   # Intro videos
├── components/                   # Reusable components
├── constants/                    # App constants (Colors, Styles)
├── context/                      # React contexts
├── interfaces/                   # TypeScript interfaces
└── store/                        # State management

```

## Web Compatibility Notes

This app has been optimized for web compatibility with the following changes:

1. **Dynamic App Icon**: The `expo-dynamic-app-icon` module is conditionally loaded only on native platforms (iOS/Android), as it's not supported on web.

2. **Clerk Authentication**: The app includes a fallback mode when Clerk authentication is not configured, allowing you to view the landing page without setting up authentication.

## Development Notes

- The app uses Expo Router for file-based routing
- Authentication is handled by Clerk
- The app supports both light and dark modes
- Multiple app icon variations are available (Default, Dark, Vivid)
- Biometric authentication (Face ID/Touch ID) is supported on native platforms

## Testing

```bash
npm test
```

## Known Issues

1. **Clerk Authentication Required**: Full app functionality requires a valid Clerk publishable key. The signup and login pages won't work in demo mode.

2. **Native Modules on Web**: Some features like dynamic app icons and biometric authentication are only available on native platforms.

3. **Video Background**: The landing page video may not load properly on all browsers.

## Getting a Clerk Account

To use the full authentication features:

1. Sign up for a free account at [https://clerk.com](https://clerk.com)
2. Create a new application
3. Copy your publishable key from the API Keys section
4. Add it to your `.env` file

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is for educational purposes. Please respect Revolut's trademarks and branding.

## Acknowledgments

- Inspired by Revolut's mobile app design
- Built with Expo and React Native
- Authentication powered by Clerk
