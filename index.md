---
slug: "github-contact.jnapolitano.com"
title: "contact.jnapolitano.com"
repo: "justin-napolitano/contact.jnapolitano.com"
githubUrl: "https://github.com/justin-napolitano/contact.jnapolitano.com"
generatedAt: "2025-11-23T08:23:40.643635Z"
source: "github-auto"
---


# Building contact.jnapolitano.com: A Personal Hugo Site with Data and Automation

Hey there! I wanted to share some insights into my project, `contact.jnapolitano.com`. It's a personal website built with Hugo, but it's much more than just a static site. Over time, it has evolved into a hub where I experiment with blog content, data scraping, cloud storage, and database integration — all wrapped up in a neat, automated workflow.

## Why I Started This

I needed a personal site that could showcase my projects, blog posts, and experiments. I wanted something lightweight but powerful, easy to maintain, and flexible enough to integrate with other tools I use daily. Hugo was a natural choice for its speed and simplicity.

But I also wanted to automate content updates and data gathering, so I started incorporating Python scripts to scrape RSS feeds, process data, and even connect to a MySQL database to store posts and author info. Plus, I integrated Google Cloud Storage utilities for managing assets in the cloud.

## What Problem This Solves

Managing a personal site with dynamic content can be cumbersome. Manually updating posts, syncing data, and deploying changes takes time and is prone to errors.

This project automates much of that:

- **RSS Scrapers:** Python scripts pull new posts from feeds, convert dates, and prepare data for insertion.
- **Database Integration:** Using MySQL to store posts and author metadata provides a structured backend.
- **Cloud Storage:** Google Cloud Storage client utilities help manage media and assets efficiently.
- **CI/CD Workflow:** GitHub Actions automate building the Hugo site and deploying it to GitHub Pages seamlessly.

## How It's Built

The core site is built with Hugo, using the `hermit-V2` theme. Content is organized into folders like `archived-posts`, `garbage` (for experimental posts), and `content` for active posts.

Configuration is managed with `hugo.toml`, which sets up language, theme, and site parameters.

Python scripts live inside the `public/posts` folder, handling tasks like RSS scraping (`rss-scraper.py`), database connection (`db-connector.py`), and data processing.

The MySQL schema is defined in SQL files under `public/posts/mysql-config/`, creating tables for posts, authors, and mastodon posts.

There's also a GitHub Actions workflow (`hugo.yaml`) that builds the site using Hugo and deploys it to GitHub Pages automatically on pushes to the main branch.

## Interesting Implementation Details

- **Multi-language Support:** The config includes placeholders for French and Italian, though English is the default.
- **Git Info Enabled:** Hugo's `enableGitInfo` is true, allowing the site to display last modified info based on git history.
- **RSS Feed Parsing:** The Python scripts parse RSS feeds, convert published dates to epoch time, and compare them with the last run to identify new posts.
- **Google Cloud Storage Client:** A custom Python class wraps GCS operations, supporting bucket listing and creation, which is handy for managing cloud assets.
- **Database Connector:** Uses environment variables loaded via dotenv to securely connect to MySQL.
- **Automated Deployment:** The GitHub Actions workflow installs Hugo, Dart Sass, checks out the repo with submodules, builds the site with minification, and uploads artifacts for GitHub Pages.

## Why this project matters for my career

This project is a playground where I blend web development, data engineering, and cloud computing — all critical skills in today's tech landscape. It showcases my ability to:

- Build and maintain static sites with modern tools.
- Automate workflows and data pipelines.
- Integrate cloud services and databases.
- Write clean, maintainable code in multiple languages.
- Use CI/CD pipelines for professional-grade deployments.

By sharing this project and its code, I demonstrate my versatility and commitment to continuous learning — qualities that are invaluable for any developer looking to grow their career.

Thanks for reading! If you want to check out the site or the code, head over to [contact.jnapolitano.com](https://contact.jnapolitano.com) or the [GitHub repo](https://github.com/justin-napolitano/contact.jnapolitano.com).