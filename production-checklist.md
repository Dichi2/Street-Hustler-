# Production launch checklist

## Required before public launch
- Deploy `server.js` behind HTTPS.
- Set a random `JWT_SECRET` (32+ characters).
- Set a restrictive `CORS_ORIGIN`; never use `*` in production.
- Configure SMTP (`SMTP_HOST`, `SMTP_PORT`, `SMTP_USER`, `SMTP_PASS`, `MAIL_FROM`).
- Use PostgreSQL for production scale; SQLite is the included development database.
- Put the database on persistent encrypted storage and schedule backups.
- Configure monitoring, alerting and crash reporting.
- Create a Google Play signing key and store it only in GitHub Actions secrets.
- If adding real-money purchases, implement Play Billing and server-side purchase verification before granting any items.
- Add a privacy policy, terms, age rating, support contact and account deletion flow before Play Store submission.

## Never commit
`.env`, database files, keystores, passwords, JWT secrets, SMTP passwords, API keys or service-account JSON files.
