# Energy Transfer Frontend

React 18 / Create React App frontend for the Energy Transfer application.

## Run locally

1. Install Node.js (Node 18+ recommended).
2. Copy `.env.example` to `.env`.
3. Set the Supabase URL and anon/public key.
4. Add payment/public provider configuration required by your backend.
5. Install dependencies:

```bash
npm install
```

6. Start development:

```bash
npm start
```

7. Create a production build:

```bash
npm run build
```

## Security

- Only the Supabase anon/public key belongs in this frontend.
- Never put a Supabase service-role key, VTPass secret key, BillPay secret, or other server credential in a `REACT_APP_*` variable.
- Provider credentials that require secrecy should be handled by Supabase Edge Functions or another server-side backend.
- The included `.env` is sanitized so the Supabase service-role key is not shipped with this frontend.

## Important backend dependencies

Electricity verification/purchases and payment verification use the application's existing Supabase Edge Functions and backend flows. Ensure those functions are deployed and configured before production deployment.

## Production deployment

Run:

```bash
npm run build
```

Deploy the generated `build/` directory to your static host. Configure SPA fallback/rewrite rules so routes such as `/dashboard`, `/transfer`, `/wallet`, and `/admin` resolve to `index.html`.
# EnergyShare-frontend
