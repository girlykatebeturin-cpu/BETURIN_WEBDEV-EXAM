# QuietSpace — Privacy-focused social media prototype

QuietSpace is a lightweight, multi-page social media **frontend prototype** made with plain HTML, CSS, and Vanilla JavaScript. It demonstrates a calmer, privacy-minded social experience without a backend, database, or API.

> **Important:** This is a learning/demo project, not a secure social network. It stores demo data in browser `localStorage`. Passwords are stored in plain text for the local demo and must never be real/reused passwords. Do not deploy this authentication as-is.

## Pages

- `index.html` — home feed, post composer, sorting, likes, demo posts
- `pages/login.html` — local demo login
- `pages/signup.html` — local demo account creation
- `pages/profile.html` — profile details and your posts
- `pages/explore.html` — local search across posts
- `pages/settings.html` — edit profile, export data, clear posts, delete demo data
- `pages/about.html` — purpose, principles, and limitations

## Project structure

```text
quietspace-social/
├── index.html
├── pages/
│   ├── about.html
│   ├── explore.html
│   ├── login.html
│   ├── profile.html
│   ├── settings.html
│   └── signup.html
├── src/
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── main.js
├── assets/
│   └── img/
│       └── README.md
└── README.md
```

## Run locally

1. Download and extract the ZIP file.
2. Open `quietspace-social/index.html` in a modern browser.
3. For a more realistic local development setup, open the folder in VS Code and use the **Live Server** extension, then open the local URL it provides.
4. Create an account using a **throwaway demo password**.
5. Create posts, like them, search, edit the profile, and try the data controls.

No package installation or build step is required.

## Features

- Responsive layout for desktop and mobile
- Local signup/login demonstration
- Create and delete posts
- Like/unlike posts
- Newest/oldest feed sorting
- Search posts by author, handle, or content
- Edit display name, handle, and bio
- Export the signed-in demo profile and personal posts as JSON
- Clear posts or delete all QuietSpace local demo data
- Keyboard-friendly labels, visible focus, reduced-motion support, and accessible status messages
- No external fonts, analytics, trackers, third-party scripts, API calls, or backend included

## Data model

Data is stored in the current browser origin's `localStorage`:

- `quietspace_user` — currently signed-in demo profile
- `quietspace_users` — local demo accounts
- `quietspace_posts` — demo posts and user-created posts

Clearing browser site data or using another browser/device will remove or not show this data. Local storage is not encrypted and should not be considered a secure database.

## Privacy and security notes

This prototype demonstrates **privacy-minded UI choices**, not production-grade privacy or security. A real release would require, at minimum:

- Server-side authentication and secure password hashing (e.g., Argon2id or bcrypt)
- Secure session handling, HTTPS, authorization checks, input validation, and abuse prevention
- A considered data-retention policy, deletion workflow, backups, and incident response
- A privacy threat model and independent security review
- Clear consent and privacy notices; no claim that a service is “AI-proof”
- Content moderation/reporting processes that protect users while respecting expression

Because all code runs in the browser, users can inspect and modify it. The demo's local login is only a navigation/profile convenience and is not a security boundary.

## File guide

- `index.html`: markup for the feed
- `pages/*.html`: separate static page layouts
- `src/css/style.css`: shared visual theme and responsive rules
- `src/js/main.js`: localStorage helpers, rendering, navigation, post actions, authentication demo, and settings
- `assets/img/README.md`: notes for optional local image assets

## Design idea

**QuietSpace** uses soft green, warm off-white, and rounded cards to feel calm rather than attention-grabbing. The guiding principle is that technology should support human thinking and connection, not quietly replace choice or turn personal behavior into a product.
