# How to Get Your Blog Live on GitHub Pages (Free)

## What You'll End Up With
A free, live website at: `https://YOUR-USERNAME.github.io/blog/`

Total time: ~10 minutes. No coding required beyond what's already done.

---

## Step 1: Create a GitHub Account

1. Go to [github.com](https://github.com)
2. Click **Sign Up**
3. Use your personal email (not your university one — you'll want to keep this after you graduate)
4. Choose a professional username (this will appear in your URL)
5. Verify your email

## Step 2: Create a New Repository

1. Once logged in, click the **+** icon in the top-right corner → **New repository**
2. Name it: `blog` (this becomes part of your URL)
3. Set it to **Public** (required for free GitHub Pages)
4. Check the box: **Add a README file**
5. Click **Create repository**

## Step 3: Upload Your Blog Files

1. In your new repository, click **Add file** → **Upload files**
2. Open the `blog` folder I've provided on your computer
3. **Drag and drop ALL the files and folders** into the upload area:
   - `index.html`
   - `about.html`
   - `style.css`
   - The entire `posts/` folder (with post1.html through post6.html)
   - The `images/` folder (add your images here later)
4. Scroll down, write a commit message like "Initial blog upload"
5. Click **Commit changes**

**IMPORTANT:** Make sure the files are at the ROOT of the repository, not inside a subfolder. Your repo should look like:
```
blog/
  ├── index.html       ← at the root, NOT inside another folder
  ├── about.html
  ├── style.css
  ├── posts/
  │   ├── post1.html
  │   ├── post2.html
  │   ├── post3.html
  │   ├── post4.html
  │   ├── post5.html
  │   └── post6.html
  └── images/
      └── (your images go here)
```

## Step 4: Enable GitHub Pages

1. Go to your repository's **Settings** tab (gear icon at the top)
2. In the left sidebar, click **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Under **Branch**, select **main** and leave the folder as **/ (root)**
5. Click **Save**
6. Wait 1-2 minutes, then refresh the page
7. You'll see a green banner with your live URL: `https://YOUR-USERNAME.github.io/blog/`

## Step 5: Test Your Site

1. Visit your URL in a browser
2. Click through all the pages and posts
3. Check it on your phone too (the design is responsive)
4. If anything looks wrong, you can edit files directly on GitHub (click any file → pencil icon)

---

## Adding Your Own Content

### Editing Text
1. On GitHub, navigate to the file you want to edit
2. Click the **pencil icon** (Edit this file)
3. Find the `[YOUR ...]` placeholders and replace them with your own text
4. Click **Commit changes**
5. Wait ~30 seconds for the site to update

### Adding Images
1. Prepare your images (resize to max 1200px wide for fast loading)
2. On GitHub, navigate to the `images/` folder
3. Click **Add file** → **Upload files**
4. Upload your images
5. Update the HTML to reference them. Replace:
   ```html
   <div class="image-placeholder">...</div>
   ```
   with:
   ```html
   <img src="../images/your-image-name.jpg" alt="Description of image">
   ```
   (Use `../images/` in post files, `images/` in index.html and about.html)

### Adding Your Profile Photo
1. Upload your photo as `images/profile.jpg`
2. In `about.html`, replace the placeholder div with:
   ```html
   <img src="images/profile.jpg" alt="Your Name" class="about-photo">
   ```

### Embedding a YouTube Video
In any post file, add:
```html
<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:2rem 0;">
  <iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID" 
          style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;" 
          allowfullscreen></iframe>
</div>
```
Replace `YOUR_VIDEO_ID` with the ID from the YouTube URL (the part after `v=`).

---

## Customising the Blog Name

The blog is currently called "Frame / Frame". To change it:

1. Search and replace `Frame <span>/</span> Frame` across all HTML files
2. Replace it with your preferred blog name in the same format
3. Also update the `<title>` tags in each file

---

## Troubleshooting

**Site not loading?**
- Check Settings → Pages — is the source set to "main" branch?
- Make sure `index.html` is at the root of the repo, not in a subfolder

**Images not showing?**
- Check the file path: posts use `../images/`, root pages use `images/`
- Make sure the filename matches exactly (case-sensitive)

**Changes not appearing?**
- GitHub Pages can take 1-2 minutes to update after a commit
- Try a hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)

---

## What to Submit

For your Turnitin submission, include:
1. The live URL: `https://YOUR-USERNAME.github.io/blog/`
2. Screenshots of the landing page and all 6 posts
3. Your 500-word evaluative essay
4. Your bibliography (minimum 3 published texts)
