# DEV NOTES

## Credits
- **App Editor** → Using [OpenVSCode Server](https://github.com/gitpod-io/openvscode-server) via `ghcr.io/gitpod/openvscode-server`. Huge thanks to Gitpod for providing a solid VS Code Docker image that makes Next Dev editing possible.  
- **IP Fetching** → [api.ipify.org](https://api.ipify.org), super simple and reliable API for grabbing uptime IPs.  
- **Auth & Database** → [Firebase Auth](https://firebase.google.com/docs/auth) + [Firestore](https://firebase.google.com/docs/firestore). Free, simple, and perfect for handling both app data and authentication.  
- **Unblocked Games** → Pulled from old [GitHub HTML5 game repos](https://github.com/topics/html5-game). Some run natively, others are proxied through my setup.  
- **Proxy System** → Using [Epoxy](https://github.com/titaniumnetwork-dev/epoxy), [Baremux](https://github.com/tomphttp/baremux), [Wisp](https://github.com/tomphttp/wisp), and [ScramJet](https://github.com/tomphttp/scramjet).  
  Extra credit to [Technonyte’s GitLab repo](https://gitlab.com/technonyte00/vapor/-/tree/main?ref_type=heads) for helping with the static proxy config.  
  - Bare server → [aluu.xyz/bare](https://aluu.xyz/bare)  
  - Wisp server → [anura.pro](wss://anura.pro)  
- **Ideas & Systems** → Shoutout to **Vorext** for idea testing and setup help, and for making sure I stay within boundaries (no skidding). If anything ends up too close to someone else’s work, I’ll shut it down fast.

## Contributions
- **Axenttt** → helped with unblocked games, store/item ideas, and was basically my right-hand dev the whole way.

## Project Info
- **Framework** → Built with [Next.js 14](https://nextjs.org/) + TypeScript.  
- **Database** → Firestore with snapshot listeners (to prevent spam reads/writes).  
- **Auth** → Firebase Auth (UUIDs for each user).  
- **Email** → Gmail via [Google Workspace](https://workspace.google.com/).  
- ⚠️ **AI Note**: I did use AI during development, but only for ideas and bug fixes when I got stuck. No vibe coding, no straight copy-paste.

## User Data Safety
- All user data is stored securely with per-user **encryption tokens**.  
- Emails are encrypted at rest using a 64-character database encryption key.  
- Privacy first → nothing is shared without the user’s consent.

## Dev Program
> ⚠️ These notes are out early. The dev program is not fully released yet, so things may change.  

- **App Resources** → Each user currently gets **1 app** running at a time with:  
  - 512MB RAM  
  - 25% of a CPU core (1 core base)  
  - 500MB of disk space (expandable if needed)  
- **Game Assets** → Users get access to **500+ unblocked game assets** for free (not counted toward disk usage).  
  - You can upload your own assets (games, images, auth systems, APIs, etc.)  
  - Assets can be:  
    - Free  
    - Private (team-only)  
    - Monetized for tokens/credits.  
- **Domains** →  
  - Free custom domain support.  
  - Free auto SSL for subdomains like:  
    ```
    {AppId}.{region}.apps.nxtjs.com
    ```  
- **Git** → Every project gets a private Git link (password-protected). You can share your code globally or keep it private. _(Subject to change or removal)_  
- **Databases** → Every app gets a DB:  
  - Built-in custom DB (SQLite + Socket.IO)  
  - Or external options like Firebase (more coming soon).  
- **Auth** → Multiple options for app authentication:  
  - Built-in Next Dev Auth  
  - Firebase Auth  
  - OAuth  
  - Or bring your own system.  
- **Env & Secrets** →  
  - Even static apps are safe: JS files are encrypted per-app.  
  - Hardcoding secrets is technically safe (still not recommended).  
  - Custom `.env` system available, works the same as standard `.env`.  
  
  ## Security Notes
- **API Rate Limiting** → All API endpoints are protected with rate limits to prevent spam, brute force attempts, or accidental flooding.  
- **Auth Protection** → Login sessions are tied to per-user encryption tokens. Refresh tokens rotate automatically, and failed attempts are monitored.  
- **Database Safety** → Firestore rules + custom server checks ensure users can only access their own data.  
- **File Safety** → Uploaded files are sandboxed and scanned before being used by apps.  
- **Encryption** → Every app has its own per-app encryption key for secrets, environment files, and sensitive data.  

## Limitations / Known Issues
- **CDN System** → While there’s a lot of storage available, the CDN setup is limited for now.  
  - Images *may* work but are subject to moderation once an AI system is in place.  
  - Until then, uploads are limited and not guaranteed to persist forever.  
- **App Hosting** → The whole platform currently has **64GB RAM** available.  
  - Each app requires **512MB RAM minimum**, so scaling is capped.  
  - If usage spikes too high, I’ll need to explore new ways to optimize resource usage.  

## Chat
The chat system is in early stages but already works pretty well (UI + features are still coming).  

### Planned Features
- **Admin Moderation** →  
  - Admins can delete messages, ban, mute, or kick users.  
  - Users can buy a “get out of jail” card (20k–50k monyz) if the punishment isn’t severe.  
- **Custom Channels & Groups** → Users will be able to create their own rooms with private or public settings.  
- **Emotes & Reactions** → To make chat more fun and interactive.  

### How Normal Chat Works
- Users can send text messages in public or private rooms.  
- Messages are stored in the database with timestamps + author IDs.  
- Messages update live for all participants using snapshot listeners (realtime sync).  
- Each user’s chat history is private to them unless in a shared room.  
- Moderation is layered → system checks, then admin tools.  

