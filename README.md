# LaundryMate 🧺

## WARNING: THIS ENTIRE THING IS VIBE CODED!!! PROCEED WITH CAUTION AND AT YOUR OWN RISK (ALSO, FEEL FREE TO HATE)!!!

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**A privacy-first Progressive Web App for dormitory laundry room management**  
Check machine availability, book via QR/NFC, get smart notifications, and ping users - all while maintaining anonymity.

![System Architecture](architecture-diagram.png) *High-level architecture diagram*

## Key Features
- 📱 **Zero-install PWA** - Mobile-first web app with offline support
- 🔐 **Anonymous auth** - Phone verification + fun pseudonyms (e.g., "Captain Laundry")
- 🧩 **QR/NFC integration** - Scan to book machines in physical laundry rooms
- 🔔 **Smart notifications** - Web push with SMS fallback + buffer periods
- 🏓 **Ping system** - Notify previous users about forgotten laundry
- 📊 **Real-time dashboard** - Live machine status tracking
- 🔒 **Privacy by design** - Minimal data retention, pseudonymized interactions

## Technology Stack
| Component              | Technology                          | Justification                                                                 |
|------------------------|-------------------------------------|-------------------------------------------------------------------------------|
| **Frontend**           | React + Vite PWA                    | Offline support, fast development, PWA capabilities                           |
| **Styling**            | Tailwind CSS                        | Rapid responsive UI development                                               |
| **Backend**            | Node.js (Express) on AWS Lambda     | Serverless scaling, pay-per-use cost model                                    |
| **Database**           | PostgreSQL (Supabase)               | Free tier, real-time capabilities, and built-in auth                          |
| **Notifications**      | Firebase Cloud Messaging + Twilio   | Reliable push with SMS fallback                                               |
| **Job Queue**          | BullMQ + Redis                      | Delayed notifications and buffer period handling                              |
| **Auth**               | Twilio Verify                       | Low-cost SMS verification                                                     |
| **Hosting**            | Cloudflare Pages + AWS API Gateway  | Global CDN + serverless execution                                             |

## Getting Started

### Prerequisites
- Node.js v18+
- PostgreSQL database
- Twilio account (SMS)
- Firebase project (FCM)

### Installation
```bash
# Clone repository
git clone https://github.com/your-repo/laundrymate.git
cd laundrymate

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Fill in your Twilio, Firebase, and DB credentials
