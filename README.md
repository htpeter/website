# Tufte-Style Blog

A beautiful, minimalist blog built with Jekyll and Tufte CSS, designed to showcase elegant typography and thoughtful content presentation inspired by Edward Tufte's design principles.

## Features

- **Tufte-inspired typography**: Beautiful serif fonts with careful attention to readability
- **Sidenotes and margin notes**: Place notes in the margin instead of at the bottom of the page
- **Responsive design**: Works beautifully on desktop and mobile devices
- **GitHub Pages ready**: Automatic deployment via GitHub Actions
- **Full Markdown support**: Write posts in clean, simple Markdown
- **Clean, distraction-free reading experience**

## Quick Start

### Local Development

1. **Install dependencies**:
   ```bash
   bundle install
   ```

2. **Run the development server**:
   ```bash
   bundle exec jekyll serve
   ```

3. **View your site**: Open http://localhost:4000 in your browser

### Deploying to GitHub Pages

1. **Enable GitHub Pages**:
   - Go to your repository settings
   - Navigate to "Pages" in the left sidebar
   - Under "Build and deployment", set Source to "GitHub Actions"

2. **Push to main branch**:
   ```bash
   git add .
   git commit -m "Initial blog setup"
   git push origin main
   ```

3. **Wait for deployment**: The GitHub Action will automatically build and deploy your site. Check the "Actions" tab to monitor progress.

4. **Access your site**: Your blog will be available at `https://yourusername.github.io/yourrepo/`

## Configuration

Edit `_config.yml` to customize your blog:

```yaml
title: "Your Blog Title"
description: "Your blog description"
author: "Your Name"
email: "your.email@example.com"
```

## Writing Posts

### Creating a New Post

1. Create a new file in the `_posts` directory
2. Name it following the pattern: `YYYY-MM-DD-title-of-post.md`
3. Add front matter at the top:

```yaml
---
layout: post
title: "Your Post Title"
date: 2026-01-01
author: "Your Name"
excerpt: "A brief description of your post"
---
```

4. Write your content using Markdown

### Tufte CSS Features

#### Sidenotes

Add numbered sidenotes that appear in the margin:

```html
Regular text here<label for="sn-id" class="margin-toggle sidenote-number"></label>
<input type="checkbox" id="sn-id" class="margin-toggle"/>
<span class="sidenote">Your sidenote text here.</span>
```

#### Margin Notes

Add unnumbered margin notes:

```html
<label for="mn-id" class="margin-toggle">⊕</label>
<input type="checkbox" id="mn-id" class="margin-toggle"/>
<span class="marginnote">Your margin note here.</span>
```

#### New Thought (Small Caps)

Start a section with small caps:

```html
<span class="newthought">Your opening words</span> continue with regular text...
```

#### Full-Width Content

Make tables or other content span the full width:

```html
<div class="fullwidth">
Your wide content here (tables, images, etc.)
</div>
```

#### Code Blocks

Use standard Markdown code blocks:

````markdown
```python
def hello():
    print("Hello, world!")
```
````

Or inline code: `` `const x = 42;` ``

## Project Structure

```
.
├── _config.yml           # Jekyll configuration
├── _layouts/             # HTML layouts
│   ├── default.html      # Base layout
│   └── post.html         # Blog post layout
├── _posts/               # Your blog posts
│   └── YYYY-MM-DD-title.md
├── assets/
│   └── css/
│       └── tufte.css     # Tufte CSS styles
├── index.md              # Home page
├── archive.md            # Archive page
├── .github/
│   └── workflows/
│       └── jekyll.yml    # GitHub Pages deployment
└── Gemfile               # Ruby dependencies
```

## Customization

### Fonts

By default, Tufte CSS uses ET Book, a Bembo-like font. To use system fonts instead, modify the `font-family` in `assets/css/tufte.css`:

```css
body {
  font-family: Palatino, "Palatino Linotype", Georgia, serif;
}
```

### Colors

The default background is a warm off-white (`#fffff8`). To customize, edit the colors in `assets/css/tufte.css`.

### Navigation

Add or modify navigation links in `_layouts/default.html`.

## Troubleshooting

### Build fails on GitHub Actions

- Check the Actions tab for error details
- Ensure your `Gemfile` dependencies are correct
- Verify that GitHub Pages is enabled in repository settings

### Styles not loading

- Check that `baseurl` is set correctly in `_config.yml`
- Clear your browser cache
- Verify the CSS file exists at `assets/css/tufte.css`

### Sidenotes not appearing

- Ensure each sidenote has a unique ID
- Check that the margin-toggle input and label are properly connected
- On mobile, sidenotes become toggleable—tap the number to show/hide

## Credits

- Design inspired by [Edward Tufte's](https://www.edwardtufte.com) visual design principles
- CSS based on [Tufte CSS](https://edwardtufte.github.io/tufte-css/) by Dave Liepmann
- Built with [Jekyll](https://jekyllrb.com/)

## License

Feel free to use this template for your own blog. Attribution appreciated but not required.
