---
slug: github-contact-jnapolitano-com-note-technical-overview
id: github-contact-jnapolitano-com-note-technical-overview
title: contact.jnapolitano.com
repo: justin-napolitano/contact.jnapolitano.com
githubUrl: https://github.com/justin-napolitano/contact.jnapolitano.com
generatedAt: '2025-11-24T18:33:19.994Z'
source: github-auto
summary: >-
  This repo is for my personal website built with Hugo. It showcases blog posts,
  projects, and other content. Here's how to get started:
tags: []
seoPrimaryKeyword: ''
seoSecondaryKeywords: []
seoOptimized: false
topicFamily: null
topicFamilyConfidence: null
kind: note
entryLayout: note
showInProjects: false
showInNotes: true
showInWriting: false
showInLogs: false
---

This repo is for my personal website built with Hugo. It showcases blog posts, projects, and other content. Here's how to get started:

### Features
- **Hugo** for static site generation.
- Multi-language support (English, French, Italian).
- Blog management with archetypes.
- Automation scripts in Python for RSS updates and MySQL interactions.
- CI/CD pipeline via GitHub Actions.

### Getting Started

1. Clone the repo:
   ```bash
   git clone https://github.com/justin-napolitano/contact.jnapolitano.com.git
   cd contact.jnapolitano.com
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up MySQL in a `.env` file:
   ```env
   DB_USER=yourusername
   DB_PASSWORD=yourpassword
   DB_HOST=localhost
   DB_NAME=yourdbname
   ```

4. Run locally:
   ```bash
   hugo server
   ```
   Navigate to `http://localhost:1313` to see it.

### Gotchas
Make sure to have Hugo and MySQL installed, plus Google Cloud credentials for cloud features.
