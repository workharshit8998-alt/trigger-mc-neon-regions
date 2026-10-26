# Trigger MC Tierlist

A static Minecraft PvP leaderboard using Supabase.

## Deploy to Netlify

1. Keep `index.html`, `config.js`, `logo.png`, and the SVG files together in the published site directory.
2. Deploy the folder (or its ZIP contents) to Netlify.
3. Confirm the Supabase project permits the intended public `SELECT` access to the `players` table through a narrowly scoped Row Level Security (RLS) policy.

## Configuration

Edit `config.js` to set `SUPABASE_URL` and `SUPABASE_ANON_KEY`. A Supabase publishable/anon key is designed for client-side use, but database access must still be protected with RLS. Never put a service-role key, database password, or private API token in this public website.

## Notes

- The overall points are calculated from the tier values in `index.html`.
- Usernames and other database values are rendered with safer text/HTML handling.
- The leaderboard has a responsive mobile layout and keyboard-accessible profile cards.
- `style.css` is retained from the original project but `index.html` currently uses its embedded stylesheet.
