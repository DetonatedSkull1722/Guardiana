# Note: This repository is currently under security maintanance till 25th May 2025
### You will not be able to view any files, but feel free to read the context in this readme.md
# Guardianìa

Guardianìa is a mobile and web application dedicated to empowering the girl child by providing comprehensive safety, legal, and informational support. The app features real-time risk mapping, secure data management, and access to legal resources to help women and girls navigate both urban and rural environments safely.

---

## Table of Contents

1. [Features](#features)
2. [Architecture & Tech Stack](#architecture--tech-stack)
3. [Installation](#installation)
4. [Configuration](#configuration)
5. [Usage](#usage)
6. [Contribution Guidelines](#contribution-guidelines)
7. [License](#license)
8. [Contact](#contact)

---

## Features

- **Security Alerts & SOS**: 
  - One-tap SOS button to send distress alerts to pre-selected emergency contacts.
  - Geo-located push notifications when users enter high-risk zones.

- **Risk Map with Color-Coded Zones**:  
  - Interactive map displaying red (high risk), orange (moderate risk), yellow (low risk), and green (safe) zones.
  - Data-driven heatmaps sourced from community reports and official crime statistics.

- **Data Management**:  
  - Secure user profiles with encrypted personal and emergency contact information.
  - Activity logs for check-ins, alerts, and legal resource accesses.

- **Legal Information Hub**:  
  - Comprehensive database of women’s rights, local laws, and contact details of legal aid centers.
  - Step-by-step guides on filing complaints, obtaining protection orders, and accessing shelters.

- **Community Reporting**:  
  - Anonymous incident reporting to help update risk zones in real time.
  - Community moderation dashboard for reviewing and verifying reports.

- **User Roles & Admin Panel**:  
  - Role-based access for users, community moderators, and administrators.
  - Admin dashboard for managing user reports, moderating content, and updating zone classifications.

---

## Architecture & Tech Stack

| Layer             | Technologies                          |
| ----------------- | ------------------------------------- |
| Frontend (Mobile) | Flutter                               |
| Frontend (Web)    | React.js + Tailwind CSS               |
| Backend           | Node.js + Express.js                  |
| Database          | MongoDB (Atlas)                       |
| Real-time & Maps  | Socket.io, Mapbox GL JS / Google Maps|
| Authentication    | JWT, OAuth 2.0 (Google, Facebook)     |
| Hosting & CI/CD   | AWS (EC2, S3), GitHub Actions         |
| Notifications     | Firebase Cloud Messaging (FCM)        |
| Analytics         | Google Analytics, Mixpanel            |

---

## Installation

### Prerequisites

- Node.js v16+
- npm or yarn
- Flutter SDK (for mobile)
- MongoDB Atlas account or local MongoDB instance

### Clone Repository
```bash
git clone https://github.com/DetonatedSkull1722/guardiana.git
cd guardiana
```

### Backend Setup
```bash
cd backend
npm install
cp .env.example .env
# Edit .env with your MongoDB URI, JWT secret, Mapbox/Google Maps API keys, FCM credentials
npm run dev
```

### Web Frontend Setup
```bash
cd ../web
npm install
npm start
```

### Mobile App Setup
```bash
cd ../mobile
flutter pub get
# Android
flutter run -d android
# iOS (macOS only)
flutter run -d ios
```

---

## Configuration

1. **Environment Variables** (.env in `backend`):
   - `MONGODB_URI` – Your MongoDB connection string.
   - `JWT_SECRET` – Secret key for JWT token generation.
   - `MAPBOX_API_KEY` / `GOOGLE_MAPS_API_KEY` – API key for map services.
   - `FCM_SERVER_KEY` – Server key for push notifications.

2. **Map Data Sources**:
   - Configure community report webhook endpoint in `backend/config/mapConfig.js`.

3. **Roles & Permissions**:
   - Modify `roles` schema in `backend/models/User.js` to add or remove access levels.

---

## Usage

1. Register or log in via email, Google, or Facebook.
2. Set emergency contacts and location-sharing preferences in Profile.
3. View the interactive risk map and plan routes through safer zones.
4. Tap the SOS button in emergencies to notify contacts and authorities.
5. Browse legal resources and community-reported incidents.

---

## Contribution Guidelines

We welcome contributions! Please follow these steps:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/YourFeature`.
3. Commit your changes: `git commit -m "feat: describe your feature"`.
4. Push to the branch: `git push origin feature/YourFeature`.
5. Open a Pull Request describing your changes.

Please adhere to the [Code of Conduct](./CODE_OF_CONDUCT.md) and [CONTRIBUTING.md].

---

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

---

## Contact

Created by **NeuronCrafters** – [Mail](mailto:pillaikiran88@gmail.com)

Project Link: [https://github.com/DetonatedSkull1722/guardiana](https://github.com/DetonatedSkull1722/guardiana)
