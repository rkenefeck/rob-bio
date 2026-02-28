# rob.kenefeck.com

Personal website for Rob Kenefeck — cloud native practitioner, speaker, CNCF Ambassador, and Toastmaster.

Live at: **[rob.kenefeck.com](https://rob.kenefeck.com)**

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire website — all HTML, CSS, and content in one file |
| `CNAME` | Tells GitHub Pages to serve the site at `rob.kenefeck.com` |

---

## How to add a new Talk

Open `index.html` and find the `<!-- TALKS -->` section. Copy an existing talk row and paste it in the right chronological position (newest at the top):

```html
<div class="talk-row">
  <div class="talk-year">2026</div>
  <div class="talk-content">
    <div class="talk-title">Your Talk Title Here</div>
    <div class="talk-meta"><span class="event">Conference Name</span> · City, Country</div>
  </div>
  <div class="talk-links">
    <a href="https://youtube.com/..." target="_blank" rel="noopener" class="talk-link talk-link-recording">&#x25B6; Recording</a>
    <a href="https://slides.com/..." target="_blank" rel="noopener" class="talk-link talk-link-slides">&#x2197; Slides</a>
  </div>
</div>
```

**Link types — use the right class:**

| Class | When to use |
|-------|------------|
| `talk-link-recording` | YouTube or video link (dark green button) |
| `talk-link-slides` | Slides, conference details page (outline button) |
| `talk-link-placeholder` | No recording/slides available (greyed out, not clickable) |

For a talk with no links yet, replace the `<a>` tag with:
```html
<span class="talk-link talk-link-placeholder">No recording</span>
```

---

## How to add a new Blog Post

Open `index.html` and find the `<!-- BLOG -->` section. Copy an existing blog card and paste it before the LinkedIn card (which should always stay last):

```html
<a href="https://your-post-url.com" target="_blank" rel="noopener" class="blog-card">
  <div class="blog-card-tag">Topic · Platform · Mon YYYY</div>
  <div class="blog-card-title">Your Post Title</div>
  <div class="blog-card-excerpt">A one or two sentence summary of what the post is about.</div>
  <div class="blog-card-footer">Read on Platform &rarr;</div>
</a>
```

---

## How to update Contact / Social links

Search `index.html` for the `<footer>` tag. Update the `href` values for LinkedIn, YouTube, GitHub, and email as needed.

---

## DNS Setup

The following DNS record needs to exist at your domain registrar for `kenefeck.com`:

| Type | Name | Value |
|------|------|-------|
| CNAME | rob | rkenefeck.github.io |

GitHub handles HTTPS automatically once the DNS record propagates (usually within a few minutes, up to 24 hours).

---

## GitHub Pages Settings

- **Source:** Deploy from branch
- **Branch:** `main`
- **Folder:** `/ (root)`
- **Custom domain:** `rob.kenefeck.com`
- **Enforce HTTPS:** ✅ Yes (enable once DNS has propagated)
