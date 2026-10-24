# GameTrack

**GameTrack** is a full‑stack web platform for discovering, booking, and reviewing sports turfs across India.

## Architecture

| Layer | Tech |
|-------|------|
| Frontend | React 19, Vite 6, Tailwind 4, GSAP, Mapbox GL, SWR, Recharts |
| Admin panel | React 19 + Vite (separate UI for turf owners) |
| Backend | Node 20, Express 5, Mongoose (MongoDB), JWT, Bcrypt, Cloudinary, Twilio, Razorpay, node‑cron |
| Database | MongoDB (self‑hosted or Atlas) |
| CI/CD | Vercel configuration (`vercel.json`) |

## Quick Start (local development)

> **Prerequisites**: Node ≥ 20, npm ≥ 10, a MongoDB instance (local or Atlas).

```bash
# 1. Clone the repo (already done)
cd C:/Users/Shree/Downloads/gametrack-main/gametrack-main
```

### Backend
```bash
cd backend
cp .env.example .env   # create .env and fill in required variables (see list below)
npm install
npm run dev            # starts on $PORT or 10000
```

### Frontend
```bash
cd ../frontend
npm install
npm run dev            # Vite dev server (http://localhost:5173)
```

### Admin panel (optional)
```bash
cd ../admin
npm install
npm run dev            # http://localhost:5174
```

## Environment Variables
The application reads all configuration from environment variables. **Do not commit `.env` files** – they are ignored by `.gitignore`.

| Variable | Description |
|----------|-------------|
| `MONGODB_URI` | MongoDB connection string |
| `JWT_SECRET` | Secret for signing JWT tokens |
| `ADMIN_EMAIL`, `ADMIN_PASSWORD` | Default admin credentials |
| `CLOUD_NAME`, `CLOUDINARY_API`, `CLOUDINARY_SECRET` | Cloudinary credentials |
| `RAZORPAY_KEY_ID`, `RAZORPAY_SECRET`, `RAZORPAY_WEBHOOK_SECRET` | Razorpay payment gateway |
| `TWILIO_ACCOUNT_SID`, `TWILIO_AUTH_TOKEN`, `TWILIO_PHONE_NUMBER`, `TWILIO_WHATSAPP_NUMBER`, `TWILIO_BOOKING_SID`, `TWILIO_CONTENT_SID`, `TWILIO_CAMPAIGN_SID` | Twilio SMS/WhatsApp integration |
| `ONESIGNAL_APP_ID` | OneSignal push notifications |
| `VITE_BACKEND` (frontend) | URL of the backend API |
| `VITE_MAPTOKEN` (frontend) | Mapbox access token |
| `VITE_RAZORPAY_KEY_ID` (frontend) | Razorpay key ID for the client side |
| `TURF_ID` (backend) | Identifier of the single turf the app serves |
| `PORT` | Port for the backend server (default 10000) |

> **Note**: Refer to the existing `backend/.env.example` (if present) or the code for additional variables.

## Attribution
The original source code is authored by **Shravan Doijad** and is hosted at https://github.com/ShravanDoijad/gametrack. This repository is a fork for personal portfolio purposes. All original code is retained unchanged; no rewrites have been performed. Contributions are attributed to the original author.

## License
The upstream project does not contain an explicit license file. Until permission is obtained from the original author, this repository is kept **private**. Please contact the author for licensing details before redistributing.

---
*Prepared for inclusion in the personal GitHub portfolio of Yuvraj220705.*
