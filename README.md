# Negosyo Ledger

A shared bookkeeping app for a small business: daily sales and expenses, profit by week and month, a monthly cost planner with cost per unit, a price calculator, charts, and Philippine tax estimates.

- Hosted on GitHub Pages straight from this repo (`index.html`, no build step).
- Records are stored in Supabase (project `negosyo-ledger`), so everyone signed in sees the same entries. Only emails listed in the `ledger_members` table can read or write.
- The key in `index.html` is Supabase's public (anon) key. It is meant to be in the page; the database rules are what keep the data private.

## Adding a person
1. Supabase dashboard → Authentication → Users → Add user → Create new user (tick Auto Confirm).
2. Add their email to the `ledger_members` table.
