# InfraPulse - Personal Tech Blog

A professional Jekyll-based tech blog for GitHub Pages, featuring a modern UI, blog posts, tags, search functionality, and more.

## Features

- 🎨 **Modern & Clean Design**: Professional UI with dark/light mode support
- 📱 **Responsive**: Mobile-first design that works on all devices
- 🔍 **Search**: Client-side search functionality for all blog posts
- 🏷️ **Tags**: Organize posts with tags and browse by topic
- 📝 **Markdown Support**: Write posts in Markdown with syntax highlighting
- ⚡ **Fast**: Optimized for performance with minimal dependencies
- ♿ **Accessible**: Semantic HTML and proper ARIA labels
- 🔎 **SEO-Friendly**: Meta tags, structured data, and sitemap

## Setup

### Prerequisites

- Ruby 3.1 or higher
- Bundler gem

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/infrapulse.git
   cd infrapulse
   ```

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Build the site locally:
   ```bash
   bundle exec jekyll serve
   ```

4. Open your browser and navigate to `http://localhost:4000`

## Writing Posts

### Creating a New Post

1. Create a new file in the `_posts/` directory
2. Name it using the format: `YYYY-MM-DD-post-title.md`
3. Add front matter at the top:

```yaml
---
layout: post
title: "Your Post Title"
date: 2024-01-15
author: Your Name
tags:
  - Tag1
  - Tag2
---
```

4. Write your content in Markdown below the front matter

### Post Front Matter Options

- `layout`: Should be `post`
- `title`: The post title (required)
- `date`: Publication date in `YYYY-MM-DD` format (required)
- `author`: Author name (optional, defaults to site author)
- `tags`: Array of tags for the post (optional)
- `excerpt`: Custom excerpt (optional, auto-generated if not provided)

## Customization

### Site Configuration

Edit `_config.yml` to customize:
- Site title and description
- Author information
- Social media links
- Navigation menu
- Pagination settings

### Styling

The main stylesheet is located at `assets/css/main.scss`. You can customize:
- Colors (CSS variables in `:root`)
- Typography
- Spacing
- Layout

### Navigation

Edit `_data/navigation.yml` to modify the navigation menu.

## Deployment

### GitHub Pages

1. Push your code to a GitHub repository
2. Go to repository Settings → Pages
3. Select the source branch (usually `main` or `master`)
4. GitHub Pages will automatically build and deploy your site

### Custom Domain

1. Add a `CNAME` file to the root with your domain name
2. Configure DNS records as per GitHub Pages documentation
3. Update the `url` in `_config.yml` to your custom domain

## Project Structure

```
infrapulse/
├── _config.yml          # Site configuration
├── _data/               # Data files (navigation, etc.)
├── _includes/           # Reusable components
├── _layouts/            # Page layouts
├── _posts/              # Blog posts
├── assets/              # CSS, JS, and images
│   ├── css/
│   └── js/
├── .github/             # GitHub Actions workflows
└── README.md            # This file
```

## Technologies Used

- **Jekyll 4.x**: Static site generator
- **Liquid**: Templating language
- **SASS**: CSS preprocessor
- **Vanilla JavaScript**: No frameworks for simplicity
- **GitHub Pages**: Hosting

## Plugins

- `jekyll-feed`: RSS feed generation
- `jekyll-sitemap`: Sitemap generation
- `jekyll-seo-tag`: SEO optimization

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

For issues, questions, or suggestions, please open an issue on GitHub.

---

**Happy Blogging!** 🚀
