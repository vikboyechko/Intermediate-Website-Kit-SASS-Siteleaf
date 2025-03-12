# Code Stitch Jekyll Template for Siteleaf

A simple, clean Jekyll template designed to work with Siteleaf CMS. This template provides a solid foundation for building websites with Jekyll and Siteleaf, with a focus on simplicity and ease of use.

## Features

- Fully responsive design
- Clean, semantic HTML
- SASS/SCSS for styling
- Collection-based content management
- SEO optimized
- Siteleaf CMS integration
- Blog functionality
- Contact form

## Getting Started

### Prerequisites

- Ruby (version 2.5.0 or higher)
- Bundler
- Jekyll

### Installation

1. Clone this repository
```
git clone https://github.com/yourusername/jekyll-siteleaf-template.git
```

2. Navigate to the project directory
```
cd jekyll-siteleaf-template
```

3. Install dependencies
```
bundle install
```

4. Run the development server
```
bundle exec jekyll serve
```

5. Open your browser and navigate to `http://localhost:4000`

## Siteleaf Setup

1. Create a new site in Siteleaf
2. Connect your GitHub repository
3. Configure your site settings
4. Start editing your content

## Directory Structure

```
.
├── _data/              # Data files
├── _includes/          # Reusable components
├── _layouts/           # Page layouts
├── _pages/             # Pages
├── _posts/             # Blog posts
├── _portfolio/         # Portfolio items
├── _services/          # Services
├── _testimonials/      # Testimonials
├── _sass/              # SASS files
├── assets/             # Static assets
│   ├── css/            # Compiled CSS
│   ├── images/         # Images
│   ├── js/             # JavaScript
│   └── svgs/           # SVG files
├── _config.yml         # Site configuration
├── Gemfile             # Ruby dependencies
├── index.html          # Homepage
└── README.md           # This file
```

## Customization

### Site Configuration

Edit the `_config.yml` file to customize your site settings:

```yaml
title: "Your Site Title"
description: "Your site description"
url: "https://yourdomain.com"
```

### Content Management

This template uses Jekyll collections to organize content:

- **Pages**: Regular pages like Home, About, Contact
- **Posts**: Blog posts
- **Services**: Service offerings
- **Portfolio**: Portfolio items
- **Testimonials**: Customer testimonials

Each collection can be managed through the Siteleaf admin interface.

### Styling

The template uses SASS for styling. The main SASS files are located in the `_sass` directory.

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.

## Acknowledgments

- [Jekyll](https://jekyllrb.com/)
- [Siteleaf](https://www.siteleaf.com/)
- [Code Stitch](https://www.codestitch.app/)
