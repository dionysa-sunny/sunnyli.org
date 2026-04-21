# Sunny Li — personal website

Plain HTML/CSS, zero build step. Works in any browser, deploys anywhere.

## Files

- `index.html` — the single-page site (sections: intro, research, working papers, teaching, CV, contact)
- `style.css` — Stanford palette, Source Serif Pro + Source Sans Pro
- `cv.pdf` — drop your CV here (filename referenced by the download link)
- `photo.jpg` — add a headshot and replace the `photo-placeholder` div in `index.html`

## Preview locally

```bash
cd ~/Dropbox/PhD_Stanford/personal_website
python3 -m http.server 8000
# then open http://localhost:8000
```

Or just double-click `index.html`.

## Deploy

### Option A: GitHub Pages (free, username.github.io)
1. Create repo `sunnyli-NYU.github.io` (or whatever your GH handle is, ending in `.github.io`).
2. Copy the folder contents in, push to `main`.
3. Site live at `https://<handle>.github.io` within a minute.

### Option B: Stanford personal pages
Stanford provides `https://<sunetid>.people.stanford.edu/`. Upload via AFS or the web-based tool.

### Option C: Netlify drag-and-drop
Go to app.netlify.com, drop the folder, done. Free subdomain or connect a custom one.

## Things to fill in

- Replace the `dionysus@stanford.edu` email if preferred.
- Add a headshot at `assets/photo.jpg`, replace the placeholder div in `index.html`:
  ```html
  <div class="photo-block">
    <img src="assets/photo.jpg" alt="Sunny Li" class="photo">
  </div>
  ```
  and add this to CSS:
  ```css
  .photo { width: 160px; height: 200px; object-fit: cover; border: 1px solid var(--rule); }
  ```
- Drop `cv.pdf` in `assets/`.
- Swap the placeholder Google Scholar link for your actual one.
- Fill the `<a href="#">` placeholders in the Glass Ceiling paper section with real PDF / slides links.
