# Calldex — Contact Manager (Legacy React Demo)

A small React contact-management project featuring a contact list, forms, and browser-local persistence. This repository is preserved as a **learning project**, not a production-ready customer database or authentication system.

## What the source contains

- Create, view, edit, and delete contacts with name, phone number, and email fields.
- Persist contacts in the browser using `localStorage`; there is no server database or synchronization.
- Pages for Home, Contacts, and Login, routed with React Router.
- A UI built with React, Ant Design, Zustand (dependency), and `uuid` for contact identifiers.

## Run locally

Requires Node.js and npm.

```bash
npm install
cp .env.example .env
npm start
```

On Windows, copy `.env.example` to `.env` manually. Update the **sample-only** values in your local `.env` if you want to try the login form. React Scripts typically serves the app at `http://localhost:3000`.

## Security and data limitations

**Important: this is a front-end demonstration, not secure authentication.**

- The login comparison runs in the browser and reads `REACT_APP_*` variables. Values with this prefix are included in the client bundle and **must never be treated as secrets**.
- The authenticated state is stored in `localStorage`. It does not provide server-enforced access control.
- Contacts are also stored in `localStorage`; do not enter personal, confidential, or production customer information.
- An earlier version committed a local `.env` file. Removing it from the latest revision **does not erase Git history**. Any values previously used elsewhere should be rotated.

To build a deployable contact manager, replace this mechanism with server-side authentication, access controls, and storage appropriate to the use case.

## Scope

This repository documents an earlier learning exercise. For newer client-oriented automation, API, and data-processing demonstrations, see [Freelance Solutions Portfolio](https://github.com/WellingtonMax/freelance-solutions-portfolio).
