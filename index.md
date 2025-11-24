---
slug: github-contact.jnapolitano.com
title: 'contact.jnapolitano.com: Hugo Site with Python Automation and MySQL Backend'
repo: justin-napolitano/contact.jnapolitano.com
githubUrl: https://github.com/justin-napolitano/contact.jnapolitano.com
generatedAt: '2025-11-23T08:45:09.849566Z'
source: github-auto
summary: >-
  Description of a personal Hugo static site using Python scripts for RSS ingestion, MySQL metadata
  management, and automated GitHub Actions deployment.
tags:
  - hugo
  - python
  - mysql
  - static-site
  - automation
  - github-actions
seoPrimaryKeyword: hugo static site
seoSecondaryKeywords:
  - python automation
  - mysql metadata
  - github actions deployment
seoOptimized: true
topicFamily: automation
topicFamilyConfidence: 0.9
topicFamilyNotes: >-
  The post centers on automating content ingestion, metadata management, and deployment using Python
  scripts, MySQL, and GitHub Actions. While it involves Hugo static site generation, the main
  distinguishing focus is on automation workflows and deployment pipelines rather than purely static
  site content.
---

# Project Overview: contact.jnapolitano.com

This project is a personal website built using the Hugo static site generator. It serves as a platform to publish blog posts, showcase projects, and manage content efficiently. The repository contains not only the Hugo site source but also Python scripts for automating content ingestion and database management, along with deployment workflows.

## Motivation and Problem Statement

Static site generators like Hugo offer fast, secure, and maintainable websites. However, managing dynamic content such as blog posts sourced from RSS feeds or integrating with external data stores requires additional tooling. This project addresses the challenge of automating content updates, managing metadata in a relational database, and deploying the site seamlessly.

## Architecture and Implementation Details

### Hugo Site

The core of the project is a Hugo-based static website. The site supports multiple languages, with English as the default. Content is organized under `content/` and `archived-posts/` directories, using Hugo archetypes for consistent post formatting. The site uses the "hermit-V2" theme, configured via `config.toml` and `hugo.toml` files.

### Python Automation Scripts

Several Python scripts automate content management:

- **RSS Feed Scraping:** Scripts parse RSS feeds from the live site or external sources to detect new posts. They convert publication dates to epoch timestamps to determine if new content has appeared since the last run.

- **MySQL Database Interaction:** Using the `mysql.connector` library, scripts connect to a MySQL database to insert or update metadata about posts and authors. Environment variables configure the database connection.

- **Google Cloud Storage Client:** A Python class wraps Google Cloud Storage SDK functionality to list and create buckets, enabling cloud asset management.

These scripts enable a workflow where new blog posts detected via RSS are programmatically recorded in the database, supporting further automation such as social media updates or content indexing.

### Database Schema

The database schema includes tables for `posts`, `authors`, and `mastodon_posts`. Each table uses UUIDs as primary keys stored in binary form for efficiency. The `posts` table tracks metadata such as author IDs, publish dates, descriptions, links, and titles. The `authors` table stores author names. This schema supports structured content management beyond the static files.

### Deployment

Deployment is automated with GitHub Actions. The workflow installs Hugo and Dart Sass, checks out the repository including submodules, builds the site with minification and garbage collection enabled, and deploys to GitHub Pages. This ensures that changes pushed to the main branch are reflected live with minimal manual intervention.

## Practical Considerations

- **Configuration Management:** Environment variables and `.env` files manage sensitive data like database credentials, keeping them out of source control.

- **Extensibility:** The modular design of scripts and Hugo configuration allows for adding new languages, content types, or cloud integrations.

- **Error Handling:** Python scripts include basic exception handling to raise errors, but further robustness could be added.

- **Testing:** There is no explicit testing framework present; adding tests would improve reliability.

## Summary

This project exemplifies a pragmatic approach to managing a personal static website with dynamic content ingestion and backend metadata management. It leverages Hugo for site generation, Python for automation, MySQL for structured data, and cloud services for asset storage. The deployment pipeline ensures continuous delivery. The design choices favor simplicity, maintainability, and automation, supporting ongoing content updates with minimal manual effort.


