# Wazanin Website - Jekyll Version

A modern recruitment website built with Jekyll, connecting Ethiopian talent to Saudi employers.

## Features

- Responsive design
- Modern UI with smooth animations
- SEO optimized
- Fast loading times
- Easy to maintain and update

## Prerequisites

Before you begin, ensure you have the following installed:

- **Ruby** (version 2.5.0 or higher)
- **RubyGems**
- **GCC** and **Make** (for compiling native extensions)

### Installing Ruby on Windows

1. Download and install Ruby from [RubyInstaller](https://rubyinstaller.org/)
2. Make sure to check "Add Ruby executables to your PATH" during installation
3. Install the MSYS2 development toolchain when prompted

### Installing Ruby on macOS

```bash
# Using Homebrew
brew install ruby

# Or using rbenv
brew install rbenv
rbenv install 3.0.0
rbenv global 3.0.0
```

### Installing Ruby on Linux (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install ruby-full build-essential
```

## Installation

1. **Clone or navigate to the project directory:**
   ```bash
   cd project/project
   ```

2. **Install Jekyll and dependencies:**
   ```bash
   bundle install
   ```

   If you don't have Bundler installed:
   ```bash
   gem install bundler
   bundle install
   ```

## Building and Running

### Development Server

To start a local development server:

```bash
bundle exec jekyll serve
```

This will:
- Start a local server at `http://localhost:4000`
- Watch for file changes and automatically rebuild
- Enable live reload (if supported by your browser)

### Build for Production

To build the site for production:

```bash
bundle exec jekyll build
```

This creates a `_site` directory with the built website.

### Build and Serve

To build and serve the site:

```bash
bundle exec jekyll serve --livereload
```

## Project Structure

```
project/
├── _config.yml          # Jekyll configuration
├── _layouts/            # Layout templates
│   └── default.html     # Default layout
├── _includes/           # Reusable components
│   ├── header.html      # Site header
│   └── footer.html      # Site footer
├── assets/              # Static assets
│   ├── css/
│   │   └── main.css     # Main stylesheet
│   ├── js/
│   │   └── main.js      # Main JavaScript
│   └── images/          # Images
├── index.md             # Homepage
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

## Customization

### Adding New Pages

1. Create a new `.md` file in the root directory
2. Add front matter at the top:
   ```yaml
   ---
   layout: default
   title: Your Page Title
   description: Page description for SEO
   ---
   ```
3. Add your content below the front matter

### Modifying Styles

Edit `assets/css/main.css` to customize the appearance.

### Adding JavaScript

Edit `assets/js/main.js` to add custom functionality.

## Deployment

### GitHub Pages

1. Push your code to a GitHub repository
2. Go to repository Settings > Pages
3. Select source branch (usually `main` or `gh-pages`)
4. Your site will be available at `https://username.github.io/repository-name`

### Netlify

1. Connect your GitHub repository to Netlify
2. Set build command: `bundle exec jekyll build`
3. Set publish directory: `_site`
4. Deploy!

### Vercel

1. Connect your GitHub repository to Vercel
2. Vercel will automatically detect Jekyll and configure the build
3. Deploy!

## Troubleshooting

### Common Issues

**"bundle: command not found"**
- Install Bundler: `gem install bundler`

**"jekyll: command not found"**
- Install Jekyll: `gem install jekyll bundler`

**Build errors on Windows**
- Make sure you have the MSYS2 development toolchain installed
- Try running: `ridk install`

**Port already in use**
- Use a different port: `bundle exec jekyll serve --port 4001`

### Getting Help

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Jekyll Troubleshooting](https://jekyllrb.com/docs/troubleshooting/)
- [Ruby Installation Guide](https://www.ruby-lang.org/en/documentation/installation/)

## License

This project is licensed under the MIT License.

## Support

For support, email info@wazanin.com or create an issue in the repository.