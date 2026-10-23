# Chat

A private, mobile-first one-to-one team chat app built with Next.js, TypeScript, Tailwind CSS, and Supabase.

## Current foundation
- Premium responsive authentication and chat UI foundation.
- Supabase schema for profiles, one-to-one conversations, encrypted-message payloads, receipts, device public keys, and private PIN credential storage.
- Row Level Security enabled on app tables.
- No service-role key or other secret belongs in the browser or repository.

## Local setup
1. Install Node.js 20.9+.
2. Copy .env.example to .env.local and fill in your Supabase project URL and publishable/anon key.
3. Run npm install and npm run dev.

## Security status
The database schema is only the foundation. PIN-only authentication, server-side cooldown enforcement, conversation creation, and end-to-end encryption are not yet complete. Do not use this app for sensitive conversations until those flows are implemented and independently tested. Message payload fields are designed for ciphertext; this repository does not yet claim that E2EE is implemented.
