# Synaptry

Synaptry is a personal knowledge archive and publishing platform for exploring technology, mathematics, physics, philosophy, and other ideas through AI-assisted dialogue. The project presents a clean, static website where users can publish, read, search, and discuss posts that capture conversations with AI models and the insights they generate.

## Overview

This repository contains the frontend for a lightweight content publishing site built with plain HTML, CSS, and JavaScript. It is designed as a static web experience that connects to Firebase Realtime Database for storing posts and comments. The site is intended to feel like a digital notebook or personal archive for AI-driven thinking, technical exploration, and reflective writing.

The project is centered around a simple idea: turn AI conversations into lasting, browsable content that can be categorized, searched, and discussed over time.

## What the project does

Synaptry allows users to:

- View a landing page that introduces the project and its content categories
- Browse recent posts grouped by subject areas such as Hardware, Software, Mathematics, Physics, Philosophy, and Miscellaneous
- Open individual post pages to read full content, summaries, and metadata
- Create new posts with title, category, author, password, AI model, summary, and body content
- Edit or delete existing posts using a password-based workflow
- Leave comments and reply to comments on individual posts
- Search posts by keyword, category, title, body content, summary, or author
- Render Markdown content and mathematical expressions with support for KaTeX

## Main features

### 1. Category-based content archive
The homepage presents a set of content cards for major themes:

- Hardware
- Software
- Mathematics
- Physics
- Philosophy
- Miscellaneous

Each category is linked to a filtered post view so visitors can explore content by domain.

### 2. Post creation and editing
The writing page provides a form for publishing new posts or editing existing ones. It supports:

- Title and category selection
- Author name and password
- AI model attribution
- Summary and full post content
- Markdown input
- Preview support
- Paste conversion for copied conversation text

### 3. Full post detail view
The post detail page displays:

- Post title and metadata
- Summary block
- Full Markdown-rendered content
- A branch-like flow diagram that visualizes the conversation structure or exploration stages
- Comment and reply sections

### 4. Search functionality
The search page lets users find posts through a simple keyword-based interface with filters for:

- Category
- Title
- Content
- Summary
- Author

### 5. Commenting system
Readers can leave comments on posts and reply to existing comments. Comments are stored in Firebase alongside posts.

## Tech stack

This project uses a lightweight client-side stack:

- HTML for structure
- CSS for styling and layout
- Vanilla JavaScript for interactivity
- Firebase Realtime Database for persistence
- Marked.js for Markdown rendering
- KaTeX for mathematical expression rendering

## Project structure

The repository contains the following main files:

- index.html: homepage with categories and recent posts
- write.html: post creation and editing interface
- post.html: full post detail page with comments and flow view
- search.html: search page for filtering and finding posts
- preview.html: preview screen for draft content
- styles.css and other page-specific CSS files: styling for the website

## How it works

1. The website is served as a static frontend.
2. The browser loads the site directly from the repository or a hosting provider such as GitHub Pages.
3. Firebase is initialized in the browser with a public configuration.
4. Posts and comments are read from and written to Firebase Realtime Database.
5. The client renders post content dynamically using JavaScript, Markdown, and KaTeX.

Because the application is frontend-only, there is no traditional backend server or authentication system. Data is stored in Firebase and handled client-side.

## Local development

You can run this project locally by serving the repository with any simple static file server.

Example using Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Deployment

This project is intended to be hosted as a static website. The repository includes a CNAME file, which suggests deployment through a custom domain or GitHub Pages-style hosting.

To deploy it:

1. Upload the repository contents to your static hosting platform
2. Ensure the site can access Firebase over HTTPS
3. Optionally replace the Firebase configuration with your own project credentials

## Firebase configuration

The current implementation uses a hardcoded Firebase configuration embedded in the HTML files. If you fork or reuse this project, it is strongly recommended to:

- Create your own Firebase project
- Enable Realtime Database
- Replace the existing Firebase config values with your own
- Review database rules for security and access control

## Notes and limitations

- The interface is currently Korean, although the README is written in English.
- The site relies on client-side JavaScript and Firebase access from the browser.
- Post editing and deletion are password-protected only through client-side checks; this is suitable for a lightweight personal project but not a high-security production system.
- The project does not include a backend API, user management system, or server-side validation.

## Future possibilities

Potential enhancements for this project include:

- User authentication and account-based authoring
- Server-side moderation and admin tools
- Better SEO and metadata support
- A richer editor experience with syntax highlighting and drag-and-drop media support
- Dark/light theme switching and improved responsive design
- Full backup and export features for archived posts

## License

No explicit license file is included in the repository. If you plan to reuse or redistribute this project, please confirm the licensing terms with the original author.

## Summary

Synaptry is a simple but thoughtful platform for turning AI conversations into a durable archive of ideas. It combines a minimalist content site with Firebase-backed storage, Markdown rendering, search, comments, and category-based browsing to create a lightweight personal knowledge hub.
