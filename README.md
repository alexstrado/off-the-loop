# Off the Loop 🔄➡️

A minimal, elegant blog about breaking free from doomscrolling and reclaiming your digital attention.

## What's inside

- **5 blog posts** on practical strategies for reducing phone dependency
- **Modern, responsive design** that works on all devices
- **Dark mode support** with system preference detection
- **Single HTML file** – no build process needed
- **GitHub Pages ready** – deploy with zero configuration

## Posts included

1. **How I freed myself from doomscrolling (without deleting all my apps)** – Three simple rules that actually work
2. **What filled the time instead of my morning scroll** – Real replacement activities
3. **The 10-minute urge check** – A game-changing technique
4. **Why quitting cold turkey failed (and what worked instead)** – Honest talk about relapse and finding balance
5. **My monthly phone audit** – A repeatable system for staying intentional

## Quick Start

### Local viewing
1. Download `index.html`
2. Open it in your browser
3. Done! No server required.

### Deploy to GitHub Pages

#### Option 1: Using GitHub Pages directly (recommended)

1. Fork this repository (or create a new one)
2. Upload `index.html` to your repository root
3. Go to **Settings → Pages**
4. Under "Build and deployment," select:
   - Source: `Deploy from a branch`
   - Branch: `main` (or your default branch)
5. Save
6. Your site will be live at `https://yourusername.github.io/off-the-loop`

#### Option 2: Using a custom domain

1. Follow the same steps above
2. In **Settings → Pages**, add your custom domain
3. Update DNS records with GitHub's IP addresses (see [GitHub docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site))

### File structure for your repo

```
off-the-loop/
├── index.html          (your website)
├── README.md           (this file)
└── LICENSE             (optional: MIT recommended)
```

That's it. No build process, no dependencies.

## Customization

### Colors
Edit the CSS variables at the top of the `<style>` section:
```css
:root {
    --primary: #1a1a1a;
    --accent: #2563eb;
    --text: #1a1a1a;
    /* etc */
}
```

### Content
Edit the `posts` array in the JavaScript section at the bottom:
```javascript
const posts = [
    {
        title: "Your post title",
        meta: "5 min read • 2024",
        content: `<p>Your HTML content here</p>`
    },
    // ... more posts
];
```

### Add more posts
1. Add a new `<article class="post-card">` element in the grid
2. Add a new object to the `posts` array
3. Increment the post number and update the `onclick` index

### Fonts and typography
The site uses system fonts for maximum performance. To change:
- Edit the `font-family` in the `body` CSS rule

## Features

✨ **Light & Dark mode** – Automatically respects system preferences  
⚡ **Fast** – Single HTML file, ~15KB, no external dependencies  
📱 **Mobile-first** – Responsive design, works perfectly on all screens  
♿ **Accessible** – Semantic HTML, keyboard navigation, screen reader friendly  
🌐 **No build process** – Edit and deploy instantly  
🎨 **Beautiful** – Minimal, clean design focused on readability  

## Deployment URLs

After deploying to GitHub Pages, your blog will be available at:
- `https://yourusername.github.io/off-the-loop` (if your repo is named `off-the-loop`)
- Or your custom domain if configured

## Markdown tip

If you want to convert Markdown to HTML for your blog posts, use an online converter like:
- [Markdown to HTML](https://markdowntohtml.com/)
- Then paste the HTML into the `content` field in the `posts` array

## License

MIT – Feel free to use this template for your own projects

## Questions?

This blog is meant to be easily customizable. Edit the HTML directly in any text editor, make your changes, and push to GitHub. That's it.

---

**Off the Loop** – A project about digital wellness and intentional technology use.
