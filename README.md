<div align="center">
  <br />
  <img src="assets/readme/readme-hero.webp" alt="Recurrly — Subscription Manager" width="100%" />
  <br />

  <div>
    <img src="https://img.shields.io/badge/-React_Native-61DAFB?style=for-the-badge&logo=react&logoColor=white" />
    <img src="https://img.shields.io/badge/-NativeWind-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
    <img src="https://img.shields.io/badge/-Expo-000020?style=for-the-badge&logo=expo&logoColor=white" /><br/>
    <img src="https://img.shields.io/badge/-Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" />
    <img src="https://img.shields.io/badge/-Express-000000?style=for-the-badge&logo=express&logoColor=white" />
    <img src="https://img.shields.io/badge/-MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" /><br/>
    <img src="https://img.shields.io/badge/-Clerk-6C47FF?style=for-the-badge&logo=clerk&logoColor=white" />
    <img src="https://img.shields.io/badge/-PostHog-F0AD4E?style=for-the-badge&logo=posthog&logoColor=white" />
    <img src="https://img.shields.io/badge/-TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
  </div>

  <h2>Recurrly</h2>
  <p>A production-ready mobile app for tracking subscriptions, managing recurring expenses, and never missing a billing date.</p>
</div>

---

## 📋 Table of Contents

1. [Introduction](#introduction)
2. [Tech Stack](#tech-stack)
3. [Features](#features)
4. [Quick Start](#quick-start)
5. [Environment Variables](#environment-variables)

---

## ✨ Introduction <a name="introduction"></a>

**Recurrly** is a full-stack subscription management application that helps users monitor and control their recurring expenses from a single, clean dashboard. Built with a modern mobile-first architecture using React Native and Expo, it features subscription tracking, automated billing reminders, secure authentication, and production-grade analytics.

---

## ⚙️ Tech Stack <a name="tech-stack"></a>

### Frontend & Mobile

| Technology | Purpose |
|---|---|
| [React Native](https://reactnative.dev/) | Cross-platform native mobile app (iOS & Android) |
| [Expo](https://expo.dev/) | File-based routing, EAS builds, and dev tooling |
| [TypeScript](https://www.typescriptlang.org/) | Static typing for maintainable, error-resistant code |
| [NativeWind v4](https://www.nativewind.dev/) | Tailwind CSS utility-first styling for React Native |

### Backend & Database

| Technology | Purpose |
|---|---|
| [Node.js](https://nodejs.org/) | JavaScript runtime for the backend service |
| [Express](https://expressjs.com/) | REST API routing and middleware layer |
| [MongoDB](https://www.mongodb.com/) | NoSQL document database for user and subscription data |

### Infrastructure & Tools

| Technology | Purpose |
|---|---|
| [Clerk](https://clerk.com/) | Authentication, session management, and user profiles |
| [PostHog](https://posthog.com/) | Product analytics, event tracking, and feature flags |
| [Zustand](https://zustand-demo.pmnd.rs/) | Lightweight client-side state management |
| [Day.js](https://day.js.org/) | Date parsing and manipulation for billing logic |

---

## 🔋 Features <a name="features"></a>

- **Subscription Dashboard** — A centralized hub displaying all active and inactive recurring charges at a glance.
- **Upcoming Renewals** — A horizontal list of subscriptions renewing within the next 7 days, so you're never caught off guard.
- **Add Subscriptions** — A bottom-sheet modal to create new subscriptions with name, price, frequency, and category.
- **Expandable Cards** — Tap any subscription card to reveal full details: payment method, start date, renewal date, and status.
- **Search & Filter** — Search subscriptions by name, category, or plan across the dedicated Subscriptions tab.
- **Secure Auth** — Full sign-up, email verification, and sign-in flows powered by Clerk, with MFA support.
- **Native Tab Navigation** — A floating, rounded tab bar with pill-style active state indicators.
- **Production Analytics** — PostHog event tracking for sign-in, sign-up, subscription creation, and screen views.
- **Settings & Profile** — View account info, user ID, join date, and sign out from the Settings tab.

---

## 🤸 Quick Start <a name="quick-start"></a>

### Prerequisites

Ensure the following are installed:

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en) (v18+)
- [npm](https://www.npmjs.com/)
- [Expo Go](https://expo.dev/go) on your iOS or Android device

### Clone & Install

```bash
git clone https://github.com/adrianhajdin/react-native-recurrly.git
cd react-native-recurrly
npm install
```

### Run the Development Server

```bash
npx expo start
```

Once Metro starts, you'll see a QR code in the terminal:

| Key | Action |
|-----|--------|
| `a` | Open on Android emulator |
| `i` | Open on iOS Simulator (macOS only) |
| `w` | Open in browser (Expo Web) |
| `r` | Reload the app |
| `m` | Open developer menu |

Scan the QR code with **Expo Go** on your phone to run the app instantly — no build step required.

---

## 🔑 Environment Variables <a name="environment-variables"></a>

Create a `.env` file in the project root:

```env
EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY=
POSTHOG_PROJECT_TOKEN=
POSTHOG_HOST=https://us.i.posthog.com
```

| Variable | Where to get it |
|---|---|
| `EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY` | [Clerk Dashboard](https://dashboard.clerk.com/) → API Keys |
| `POSTHOG_PROJECT_TOKEN` | [PostHog](https://posthog.com/) → Project Settings |
| `POSTHOG_HOST` | Use `https://us.i.posthog.com` (US Cloud) or your self-hosted URL |

---

## 📁 Project Structure

```
recurrly/
├── app/
│   ├── _layout.tsx          # Root layout (Clerk + PostHog providers)
│   ├── (auth)/              # Sign-in and sign-up screens
│   ├── (tabs)/              # Main app tabs (Home, Subscriptions, Insights, Settings)
│   └── subscriptions/       # Dynamic subscription detail route
├── components/
│   ├── CreateSubscriptionModal.tsx
│   ├── SubscriptionCard.tsx
│   ├── UpcomingSubscriptionCard.tsx
│   └── ListHeading.tsx
├── constants/               # Theme colors, spacing, icons, seed data
├── lib/                     # Zustand store and utility functions
├── src/config/              # PostHog client configuration
├── assets/                  # Fonts, icons, images
└── global.css               # NativeWind v4 @theme tokens + component classes
```

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
