# Naveen Garla – Tech Notes

A technical blog and knowledge base built with [MkDocs](https://www.mkdocs.org/) and the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme.

🌐 **Live Site**: [https://naveengarla.github.io/tech-notes/](https://naveengarla.github.io/tech-notes/)

## Features

- ✨ Modern, responsive Material Design theme
- 📝 Built-in blog with full/draft support
- 🔍 Powerful search functionality
- 📡 RSS feed for blog posts
- 🎨 Syntax highlighting for code blocks
- 🌓 Light/dark mode toggle
- 🚀 Automatic deployment to GitHub Pages

## Local Development

### Prerequisites

- Python 3.7 or higher
- pip (Python package manager)

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/naveengarla/tech-notes.git
   cd tech-notes
   ```

2. **Install dependencies**
   ```bash
   pip install mkdocs-material
   pip install mkdocs-rss-plugin
   ```

3. **Run the development server**
   ```bash
   mkdocs serve
   ```

4. **Open your browser**
   
   Navigate to [http://localhost:8000](http://localhost:8000)

   The site will automatically reload when you make changes to your content.

## Creating Content

### Adding a New Blog Post

1. Create a new Markdown file in `docs/blog/posts/` with the format:
   ```
   YYYY-MM-DD-post-title.md
   ```

2. Add front matter at the top of the file:
   ```yaml
   ---
   date: 2026-02-15
   authors:
     - naveengarla
   categories:
     - Category Name
   ---
   ```

3. Write your content using Markdown
   
4. Use `<!-- more -->` to mark the excerpt break (content above this appears in the blog list)

### Adding a Regular Page

1. Create a new `.md` file in the `docs/` directory
2. Add the page to the navigation in `mkdocs.yml` under the `nav:` section

## Deployment

This site automatically deploys to GitHub Pages when you push to the `main` branch.

### How It Works

1. Push changes to the `main` branch
2. GitHub Actions workflow (`.github/workflows/deploy.yml`) triggers
3. MkDocs builds the site
4. Static files are pushed to the `gh-pages` branch
5. GitHub Pages serves the site from the `gh-pages` branch

### Manual Deployment

If you need to deploy manually:

```bash
mkdocs gh-deploy
```

This command builds the site and pushes it to the `gh-pages` branch.

## GitHub Pages Configuration

Make sure GitHub Pages is configured correctly in your repository settings:

1. Go to **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Select branch: **gh-pages**, folder: **/ (root)**
4. Save

The site will be available at: `https://naveengarla.github.io/tech-notes/`

## Project Structure

```
tech-notes/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions deployment workflow
├── docs/
│   ├── blog/
│   │   └── posts/              # Blog posts go here
│   │       └── 2026-02-15-welcome-to-my-tech-notes.md
│   └── index.md                # Home page
├── mkdocs.yml                  # MkDocs configuration
├── .gitignore
└── README.md
```

## Customization

Edit `mkdocs.yml` to customize:

- Site name, description, and author
- Theme colors and features
- Navigation structure
- Plugins and extensions
- Social links

## Tech Stack

- **[MkDocs](https://www.mkdocs.org/)** – Static site generator
- **[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)** – Beautiful theme
- **[MkDocs RSS Plugin](https://guts.github.io/mkdocs-rss-plugin/)** – RSS feed generation
- **[GitHub Actions](https://github.com/features/actions)** – CI/CD automation
- **[GitHub Pages](https://pages.github.com/)** – Free hosting

## License

Copyright © 2026 Naveen Garla. All rights reserved.

## Contact

- GitHub: [@naveengarla](https://github.com/naveengarla)
- Blog: [https://naveengarla.github.io/tech-notes/](https://naveengarla.github.io/tech-notes/)
