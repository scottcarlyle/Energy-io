# AGENTS.md - Energy-io

Shared brief for every AI tool working in this repo (Claude, ChatGPT/Codex). Keep it current.

## Scope
- This repo holds Energy-io work apps only. Do not copy code, data or keys between this repo and any other.
- Supabase: control-plane (HQ) project plus one Supabase project per client project. Never propose a single shared database.

## How to work
- Work on a branch named `claude/<task>` or `codex/<task>`. Never commit to `main`. Scott merges.
- One AI per branch. Do not edit another AI's open branch.
- Keep changes inside the app folder you were asked to work on.
- Update `REGISTER.md` when an app is added, moved, renamed or retired.
- Use plain, simple wording in UI text and docs. Metric units only.

## Secrets
- Never commit keys, tokens, passwords or service_role keys. Secrets live in the password manager vault for this bucket.
- Supabase anon/publishable keys are public by design and may go in config files.

## Architecture rules (decided 21 Aug 2026)
- Three planes: Master Console (SharePoint, admin), Project Console (SharePoint, one per project), Field apps (Netlify, one per project).
- A console is an HTML file in a SharePoint library. Management tokens, Netlify PATs, Graph secrets and service_role keys never go in a console file. The Master Console calls HQ Supabase Edge Functions, which hold the secrets.
- Auth: Entra ID (via Supabase Azure OIDC) for consoles; Supabase account + passkey for field apps.
- Templates are copied into a project at a pinned version, never live-linked.
- Biometric is a local unlock only, never a server-side factor (field apps need 30-day offline grace).
- One generic field bundle + per-project `config.json`, not a per-project build.
- UI gates: no build work behind a UI gate until Scott has signed off static screens.
