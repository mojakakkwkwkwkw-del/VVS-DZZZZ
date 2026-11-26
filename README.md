# VVS Rewards — Working Build

Arabic RTL rewards-site starter with Express and PostgreSQL. This package is a local runnable project, **not deployed online**.

## Included
- Register/login/logout (bcrypt password hashes; 10-character minimum)
- PostgreSQL persistence for accounts, balances, transactions, spin history, and redemption requests
- One-time 50 VVS signup bonus
- Server-issued spin prizes (10/50/80/100 VVS) and 15-hour cooldown
- 100,000 VVS redemption request with balance hold
- Responsive RTL frontend and opt-in sound
- Advisory transaction lock added to reduce concurrent-spin race conditions

## Run locally
1. Install Node.js 20+ and Docker
2. Copy `.env.example` to `.env`; replace secrets and database settings
3. Run `docker compose up -d postgres`
4. Run `npm install`
5. Run `npm start`
6. Visit `http://localhost:3000`

## Not ready for public launch yet
Email verification, daily ad-reward proof/callback, admin dashboard and review/refund workflow, robust CSRF protection, detailed rate limiting, tests, deployment setup, monitoring, and backups still need implementation and review. AADS ad placement must use the publisher's official embed code and should not falsely claim that an ad view was verified. Google Play rewards are manually reviewed; no gift codes are generated or automatically purchased.
