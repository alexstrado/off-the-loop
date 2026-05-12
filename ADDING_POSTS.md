# How to Add New Blog Posts to "Off the Loop"

## Step 1: Add the post card to the HTML grid

Find this section in `index.html` (around line 250-280):

```html
<section class="posts-grid">
    <article class="post-card" onclick="openModal(0)">
        <span class="post-number">01</span>
        ...
    </article>
    <!-- Add your new card here -->
</section>
```

Add a new card. Increment the post number and the `onclick` index:

```html
<article class="post-card" onclick="openModal(5)">
    <span class="post-number">06</span>
    <h3>Your new post title</h3>
    <p>A brief excerpt that hooks the reader.</p>
    <div class="post-meta">
        <span>📖 5 min read</span>
        <span>🎯 Your category</span>
    </div>
</article>
```

## Step 2: Add the post content to the JavaScript array

Find the `const posts = [...]` array near the bottom of the `<script>` section.

Add a new post object at the end:

```javascript
{
    title: "Your new post title",
    meta: "5 min read • 2024",
    content: `
        <p>Your introduction paragraph.</p>

        <h3>Your first section</h3>
        <p>Section content goes here.</p>

        <div class="highlight">
            <strong>Important quote or key point</strong><br>
            Supporting text for emphasis.
        </div>

        <h3>Your second section</h3>
        <p>More content.</p>

        <ul>
            <li>Bullet point 1</li>
            <li>Bullet point 2</li>
        </ul>
    `
}
```

## HTML elements you can use in post content

### Paragraphs
```html
<p>Text goes here.</p>
```

### Headings
```html
<h3>Section title</h3>
```

### Lists (unordered)
```html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
</ul>
```

### Lists (ordered)
```html
<ol>
    <li>First item</li>
    <li>Second item</li>
</ol>
```

### Highlighted box (for quotes or key ideas)
```html
<div class="highlight">
    <strong>Important point</strong><br>
    Supporting text or explanation.
</div>
```

### Bold text
```html
<strong>Bold text here</strong>
```

### Line break
```html
<br>
```

## Emoji suggestions for post meta tags

- 📖 Reading time
- 💡 Tips/Ideas
- 🎯 Goals/Focus
- 🛠️ Techniques/Tools
- 🚀 Progress/Growth
- 📊 Data/Systems
- 💬 Reflections
- 🔄 Habits
- ⏰ Time management
- 🧠 Mindfulness

## Example: Complete new post

**Step 1: Add card**
```html
<article class="post-card" onclick="openModal(5)">
    <span class="post-number">06</span>
    <h3>Why I stopped using Reddit</h3>
    <p>How I quit my favorite infinite scroll app and replaced it with books.</p>
    <div class="post-meta">
        <span>📖 4 min read</span>
        <span>💡 Decision</span>
    </div>
</article>
```

**Step 2: Add to posts array**
```javascript
{
    title: "Why I stopped using Reddit",
    meta: "4 min read • 2024",
    content: `
        <p>Reddit was my favorite way to waste time.</p>

        <h3>The turning point</h3>
        <p>After 5 years on the platform, I realized I was getting less value and more anxiety from it.</p>

        <div class="highlight">
            <strong>The decision:</strong><br>
            Delete the app entirely. Not just hide it—actually delete it.
        </div>

        <h3>What I replaced it with</h3>
        <ul>
            <li>Books (actual physical books)</li>
            <li>Conversations with friends</li>
            <li>Writing in my journal</li>
        </ul>

        <p>The difference was immediate.</p>
    `
}
```

## Tips

- Keep post titles concise (under 80 characters for mobile)
- Write excerpts as a single punchy sentence
- Use `<h3>` for section headers within posts (not h1 or h2)
- Break up long paragraphs into 2-3 shorter ones for readability
- Save and test locally before pushing to GitHub
- The highlight box is great for quotes, key points, or "aha" moments

## Testing

After editing `index.html`:
1. Save the file
2. Open it in your browser
3. Click on a post to make sure the modal opens and displays correctly
4. Check mobile view (right-click → Inspect → toggle device toolbar)
5. Push to GitHub when happy

---

That's it! You now have a fully functional blog without any build tools or dependencies.
