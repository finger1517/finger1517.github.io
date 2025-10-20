---
title: "Setting Up a Personal Website with Hugo and PaperMod"
date: 2024-12-16T14:30:00+08:00
draft: false
tags: ["hugo", "web-development", "tutorial", "static-site"]
categories: ["Tutorial"]
author: "finger1517"
description: "A step-by-step guide to setting up a beautiful personal website using Hugo static site generator and the PaperMod theme."
---

## 🎯 Why Hugo + PaperMod?

When I decided to create a personal website, I wanted something that was:

- **Fast**: Static sites load instantly
- **Simple**: Focus on content, not complex setup
- **Beautiful**: Clean, modern design
- **Flexible**: Easy to customize and extend

Hugo with the PaperMod theme ticked all these boxes perfectly.

## 🚀 Quick Setup Guide

### 1. Install Hugo

```bash
# On macOS
brew install hugo

# On Ubuntu/Debian
sudo apt-get install hugo

# Check installation
hugo version
```

### 2. Create Your Site

```bash
hugo new site my-website
cd my-website
```

### 3. Add PaperMod Theme

```bash
git init
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

### 4. Basic Configuration

Create `hugo.yaml`:

```yaml
baseURL: "https://yourusername.github.io/"
languageCode: "en-us"
title: "Your Name"
theme: ["PaperMod"]

params:
  author: "Your Name"
  description: "Your personal website description"

  homeInfoParams:
    Title: "Hi there 👋"
    Content: "Welcome to my personal corner of the internet."
```

### 5. Create Content

```bash
# Create homepage
echo "# Welcome to My Site" > content/_index.md

# Create a blog post
hugo new posts/hello-world.md
```

### 6. Build and Preview

```bash
# Preview locally
hugo server -D

# Build for production
hugo --minify
```

## 🎨 Customization Tips

### Theme Configuration

PaperMod offers extensive customization options:

```yaml
params:
  # Social links
  socialIcons:
    - name: github
      url: "https://github.com/yourusername"
    - name: twitter
      url: "https://twitter.com/yourusername"

  # Feature toggles
  ShowReadingTime: true
  ShowShareButtons: false
  ShowPostNavLinks: true
  ShowBreadCrumbs: true
```

### Custom CSS

Create `assets/css/custom.css` for additional styling:

```css
/* Custom styles */
.site-title {
  color: #your-color;
}
```

## 🚀 Deployment

### GitHub Pages

1. Push your Hugo source to a GitHub repository
2. Set up GitHub Actions for automatic deployment
3. Your site will be live at `https://yourusername.github.io/`

### Other Options

- **Netlify**: Great for custom domains
- **Vercel**: Excellent performance
- **AWS S3 + CloudFront**: For ultimate control

## 🛠️ Advanced Features

### Shortcodes

Hugo's shortcodes make content creation powerful:

```markdown
{{< figure src="/images/diagram.png" title="System Architecture" >}}
```

### Taxonomies

Organize content with tags and categories:

```yaml
---
title: "My Post"
tags: ["hugo", "web-dev"]
categories: ["Tutorial"]
---
```

## 📚 Resources

- [Hugo Documentation](https://gohugo.io/documentation/)
- [PaperMod Wiki](https://github.com/adityatelange/hugo-PaperMod/wiki)
- [Hugo Themes](https://themes.gohugo.io/)

## 🎉 Final Thoughts

Setting up with Hugo and PaperMod was surprisingly straightforward. The combination gives you professional results with minimal effort. The static nature means excellent performance, and the flexibility allows for endless customization as your needs grow.

Have you tried Hugo for your personal site? What challenges did you face or what tips would you add? Let me know in the comments!

---

*Happy coding!* 💻✨
