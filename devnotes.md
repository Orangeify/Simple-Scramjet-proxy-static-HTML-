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
