---
layout: post
title: "Introducing LinkSphere: A Modern Link Sharing & Networking App with React + Firebase"
date: 2025-07-05 10:12:00 +0300
categories: Projects
tags: [react, firebase, web-development, ant-design, fullstack, social-app]
author: Moshe Alper
---

Hey everyone! 👋

This week, I’m excited to share something fresh off the keyboard — **LinkSphere**. It’s a React + Firebase web app I’ve been working on, designed to let users **share links, manage their online presence, and connect professionally** — think of it as a lightweight LinkedIn for creators and devs.

And best of all? It’s live and ready to explore 👉  
[https://moshe-alper.github.io/LinkSphere/](https://moshe-alper.github.io/LinkSphere/)

## What Is LinkSphere?

At its core, **LinkSphere** is about frictionless link sharing and professional networking. I wanted to create a space where users can:
- Register/sign in securely (email or Google)
- Build and edit a personal profile
- Share and manage useful links in real time
- Discover other users and make meaningful connections

All in a clean, responsive interface powered by [React](https://reactjs.org/), [Firebase](https://firebase.google.com/), and [Ant Design](https://ant.design/).

## Why I Built It

I built LinkSphere as a hands-on learning challenge and personal portfolio piece. But also, I wanted to push myself beyond just tutorials — to go from “learning” to **launching**.

That said, I have to give major credit to the YouTube tutorial that kickstarted this project:

🎥 **Special thanks to [@CybernaticoByNishant](https://www.youtube.com/@CybernaticoByNishant)**  
🔗 [LinkedIn Clone with React & Firebase – Full Build](https://www.youtube.com/watch?v=HimR8Xtz17U)

This video gave me the foundational structure, and from there, I extended and refined the features into something uniquely mine.

## Tech Stack & Architecture

Here's a quick look under the hood:

| Tech | Purpose |
|------|---------|
| React | UI & component architecture |
| Firebase | Auth, Firestore (DB), Storage |
| Ant Design | UI components and layout |
| Sass | Custom styling |
| React Router | Client-side routing |

The app is organized around **pages** (like Login, Register, Profile, etc.), and wrapped in **layout components** that handle header/footer logic. All backend operations (auth, CRUD, etc.) are abstracted into `api/` helpers, keeping the components clean and focused on rendering.

## Key Features

- 🔐 **Authentication**: Sign up / login with email or Google
- 🙋‍♂️ **Profiles**: Add name, image, bio — build your presence
- 🔗 **Link Sharing**: Add/update/delete your own links
- 🧑‍🤝‍🧑 **Connections**: Browse the network and follow others
- 📱 **Responsive UI**: Fully mobile-friendly
- 📣 **Notifications**: Toast feedback for smooth UX

## What I Learned

Every real project teaches something new. Here are a few takeaways:

- **Firebase Auth**: Clean and easy for login systems, but managing auth state across routes takes real care (thank you `onAuthStateChanged()`).
- **Modular Styling**: Sass with Ant Design works great, but you still need to be deliberate about component-level styles vs. global tweaks.
- **State & Side Effects**: Using `useEffect` properly with Firebase subscriptions (especially Firestore listeners) can be tricky — lots of cleanup functions involved!

And most importantly: **ship it**. Even if it’s not perfect. The process of deploying and sharing a project forces you to polish things you’d otherwise ignore.

## Final Thoughts

I’m proud of how LinkSphere turned out — not just for what it does, but for how much I learned while building it. It’s a real, working app I can point to, and I hope it inspires others to turn tutorials into custom creations.

You can check out the GitHub repo here:  
[https://github.com/moshe-alper/LinkSphere](https://github.com/moshe-alper/LinkSphere)

Let me know what you think, and feel free to fork it, extend it, or use the idea for your own portfolio!

Until next time — keep building! 🚀

— Moshe
