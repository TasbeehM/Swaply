# Swaply — Community Fashion Marketplace

A full-stack starter implementation for the Swaply university project. Frontend: HTML, CSS and Vanilla JS. Backend: Node.js + Express. Database: SQLite.

## Requirements
- Node.js 18 or newer
- npm

## Run locally
1. Open a terminal in `backend`.
2. Install dependencies: `npm install`
3. Copy `.env.example` to `.env` and change `SESSION_SECRET`.
4. Add demo data: `npm run seed`
5. Start the API: `npm start`
6. Open `frontend/index.html` using VS Code Live Server (or serve the frontend on `http://localhost:5500`).

The API runs at `http://localhost:3000`. Check `http://localhost:3000/api/health`.

## Demo account
- Email: `demo@swaply.com`
- Password: `Swaply123!`

## Pages
Home, About, How It Works, Contact, Login, Sign Up, Forgot Password, Explore, Item Details, Add Item, Profile, Edit Profile, My Wardrobe, Wishlist, Messages, Notifications, My Requests, My Transactions, Reviews, Report, FAQ, Privacy Policy, Terms, 404 and Access Denied.

## Important implementation notes
- The marketplace does not process online payments. Requests and handover coordination are member-to-member.
- Authentication uses server-side sessions and bcrypt password hashing.
- Listings, wishlist, requests, transactions, conversations, messages, notifications, reviews, reports and contact messages are stored in SQLite.
- Image uploads are stored in `backend/uploads` (5 MB maximum; image MIME types only).
- Password reset UI is present, but actual email delivery is intentionally not claimed because no email provider is configured.
- The frontend contains an initial demo catalogue for immediate visual preview. The API also supports persistent listings and returns database listings; connect/use the API for production data.
- This is a functional project foundation, not a production-audited marketplace. Before public deployment, configure HTTPS, secure cookies, CSRF protection, rate limiting, robust email verification/password reset, image storage, moderation tooling and additional automated tests.

## API overview
`/api/auth`, `/api/users`, `/api/listings`, `/api/wishlist`, `/api/requests`, `/api/transactions`, `/api/conversations`, `/api/notifications`, `/api/reviews`, `/api/reports`, `/api/contact`.
