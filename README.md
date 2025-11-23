# contact.jnapolitano.com

A personal website built with Hugo, showcasing blog posts, projects, and more. This repository contains the source code and content for the site hosted at [contact.jnapolitano.com](https://contact.jnapolitano.com).

---

## Features

- Static site generator powered by [Hugo](https://gohugo.io/).
- Multi-language support (English default, with placeholders for French and Italian).
- Blog posts organized with archetypes and content folders.
- Integration of RSS feed scraping and automation scripts.
- Google Cloud Storage client utilities.
- MySQL database schema and connector scripts for post and author management.
- GitHub Actions workflow for automated deployment to GitHub Pages.

## Tech Stack

- **Hugo**: Static site generator.
- **HTML/CSS**: Site markup and styling.
- **Python**: RSS feed scraping, data processing, and MySQL interaction.
- **MySQL**: Database for storing posts and authors.
- **Google Cloud Storage SDK**: For cloud storage operations.
- **GitHub Actions**: CI/CD pipeline for deployment.

## Getting Started

### Prerequisites

- [Hugo](https://gohugo.io/getting-started/install/) installed locally.
- Python 3.x environment.
- MySQL server for database operations.
- Google Cloud credentials if using cloud storage features.

### Installation

1. Clone the repository:

```bash
git clone https://github.com/justin-napolitano/contact.jnapolitano.com.git
cd contact.jnapolitano.com
```

2. Install Python dependencies (if running Python scripts):

```bash
pip install -r requirements.txt  # Assuming a requirements file exists or install individually
```

3. Set up environment variables for MySQL connection (create a `.env` file):

```env
DB_USER=yourusername
DB_PASSWORD=yourpassword
DB_HOST=localhost
DB_NAME=yourdbname
```

### Running the Site Locally

```bash
hugo server
```

Visit `http://localhost:1313` to view the site.

### Running Python Scripts

Example: Run RSS scraper script

```bash
python public/posts/hugo-rss-mysql-update/rss-scraper.py
```

## Project Structure

```
contact.jnapolitano.com/
├── archetypes/           # Hugo archetypes for content templates
├── archived-posts/       # Older blog posts
├── assets/               # Static assets like images
├── content/              # Main site content
├── layouts/              # Hugo templates and layouts
├── public/               # Generated site output
├── resources/            # Hugo resource files
├── static/               # Static files served as-is
├── themes/               # Hugo themes (using hermit-V2)
├── garbage/              # Experimental or data-related posts
├── test/                 # Test scripts or files
├── config.toml           # Example Hugo config
├── hugo.toml             # Actual Hugo config
├── hugo.toml.example     # Config example
├── submodule.sh          # Script for git submodules
└── public/posts/          # Various Python scripts and SQL configs for data processing
```

## Future Work / Roadmap

- Improve documentation and README with detailed usage instructions.
- Add more automated tests and CI checks.
- Enhance multi-language support and localization.
- Expand integration with cloud services and database for dynamic content.
- Refine deployment workflow for smoother updates.
- Clean up and organize experimental scripts and folders.

---

*Note: Some assumptions were made about the environment and usage based on the repository structure and file contents.*