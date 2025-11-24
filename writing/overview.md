---
slug: github-contact-jnapolitano-com-writing-overview
id: github-contact-jnapolitano-com-writing-overview
title: 'Building My Personal Site with Hugo: contact.jnapolitano.com'
repo: justin-napolitano/contact.jnapolitano.com
githubUrl: https://github.com/justin-napolitano/contact.jnapolitano.com
generatedAt: '2025-11-24T17:12:32.899Z'
source: github-auto
summary: >-
  I started my GitHub project,
  [contact.jnapolitano.com](https://github.com/justin-napolitano/contact.jnapolitano.com),
  as a personal space to showcase my writing and projects. It’s all about
  keeping my online presence organized and tailored to my needs. Using Hugo, I
  created a static site that’s not just a collection of posts, but also a
  platform for future experiments and content sharing.
tags: []
seoPrimaryKeyword: ''
seoSecondaryKeywords: []
seoOptimized: false
topicFamily: null
topicFamilyConfidence: null
kind: writing
entryLayout: writing
showInProjects: false
showInNotes: false
showInWriting: true
showInLogs: false
---

I started my GitHub project, [contact.jnapolitano.com](https://github.com/justin-napolitano/contact.jnapolitano.com), as a personal space to showcase my writing and projects. It’s all about keeping my online presence organized and tailored to my needs. Using Hugo, I created a static site that’s not just a collection of posts, but also a platform for future experiments and content sharing.

## Why This Repo Exists

Honestly, in a world where I’ve got multiple projects and ideas flying around, I needed a streamlined way to present everything. This site keeps me sane. It allows me to manage my blog entries, curate my projects, and eventually share everything in a neat package. Plus, it’s a solid excuse to tinker with tech I enjoy.

## Key Design Decisions

When I designed the site, I had a few core principles in mind:

- **Simplicity**: The UI should be easy to navigate. I didn't want visitors to struggle finding content.
- **Expandability**: The option for multi-language support was a must, as I have a couple of languages I’d like to explore (French and Italian). 
- **Automation**: Automated scripts to help manage my RSS feeds and updates were essential. I don’t want to spend hours on manual updates.
- **Database Integration**: Storing metadata for posts and authors meant I could keep everything consistent and searchable.

## Tech Stack

Building this whole thing required a mix of tools and languages. Here’s what I went with:

- **Hugo**: The heart of the site for static site generation.
- **HTML/CSS**: For the front-end structure and styling.
- **Python**: Used for RSS feed scraping, MySQL interaction, and other automation scripts.
- **MySQL**: A structured approach to manage my posts and author info.
- **Google Cloud Storage SDK**: To manage and serve my assets.
- **GitHub Actions**: For CI/CD and automatic deployment to GitHub Pages.

Sticking to this stack allowed me to keep my site dynamic without the overhead of a full-fledged CMS.

## Trade-offs Made

While setting this up, I had to make some decisions that could be seen as trade-offs:

- **Static vs. Dynamic Content**: Opting for a static site means lower server costs and faster load times, but it also limits interactivity. I considered more advanced solutions, but for now, static meets my needs.
- **Library Dependency**: I chose Python for scripts, as it’s flexible. However, this introduces dependencies that have to be managed carefully.
- **Multi-language Support**: Implementing it from scratch adds complexity. While I want to expand in that direction, the additional work is a trade-off against quick changes.

## Getting Started

If you want to play around with this setup yourself, here’s how I recommend getting going:

### Prerequisites

- Install [Hugo](https://gohugo.io/getting-started/install/)
- Set up a Python 3.x environment
- A running MySQL server if you want to utilize the database features
- Google Cloud credentials for any cloud storage functionality

### Installation Steps

1. Clone the repo:
   ```bash
   git clone https://github.com/justin-napolitano/contact.jnapolitano.com.git
   cd contact.jnapolitano.com
   ```

2. Install Python dependencies (if needed):
   ```bash
   pip install -r requirements.txt
   ```

3. Set up your database connection in a `.env` file:
   ```env
   DB_USER=yourusername
   DB_PASSWORD=yourpassword
   DB_HOST=localhost
   DB_NAME=yourdbname
   ```

### Running the Site

To see everything in action, start the local server:
```bash
hugo server
```
Then, just hit `http://localhost:1313` in your browser.

### Running Scripts

For instance, if you want to run the RSS scraper:
```bash
python public/posts/hugo-rss-mysql-update/rss-scraper.py
```

## Future Work / Roadmap

I’m not done tinkering with this project. Here’s what’s next on my to-do list:

- Complete the multi-language support for French and Italian.
- Enhance the automation scripts to cover more content types and handle errors better.
- Improve the integration between RSS feeds and my database.
- Add testing and validation for the Python scripts to minimize bugs.
- Expand the cloud storage utilities for more functionality.
- Refine the Hugo theme and styling.
- Document the entire deployment process for good measure.

## Stay Updated

As I continue developing this site, I’ll be sharing updates and findings on social media. You can catch me on Mastodon, Bluesky, and Twitter/X. Follow along if you're interested in the journey!

That’s it! This is just a glimpse into my project and its future. Feel free to dive into the code on GitHub, and let me know if you have any thoughts or suggestions!
