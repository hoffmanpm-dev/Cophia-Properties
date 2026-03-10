# Cophia Properties — GitHub Pages Setup Guide

## Step 1: Create the GitHub Repository

1. Go to **github.com** → click **+** → **New repository**
2. Name it: `cophia-properties` (or whatever you prefer)
3. Set to **Public** (required for free GitHub Pages)
4. Click **Create repository**

## Step 2: Upload the Site Files

1. In your new repo, click **"uploading an existing file"** link
2. Drag and drop ALL files from this folder:
   - `index.html`
   - `CNAME`
   - (later: your `images/` folder)
3. Click **Commit changes**

## Step 3: Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages** (left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Select **main** branch and **/ (root)** folder
4. Click **Save**

## Step 4: Connect Your Custom Domain

### In GitHub:
1. On the same **Settings → Pages** screen, under **Custom domain**, type: `cophiaproperties.com`
2. Click **Save**
3. Check **Enforce HTTPS** once it becomes available

### In Zoho (your domain registrar):
You need to update your DNS records. Go to your Zoho domain management panel and set:

**Option A — If using an apex domain (cophiaproperties.com):**

| Type  | Name | Value                      |
|-------|------|----------------------------|
| A     | @    | 185.199.108.153            |
| A     | @    | 185.199.109.153            |
| A     | @    | 185.199.110.153            |
| A     | @    | 185.199.111.153            |
| CNAME | www  | YOUR-USERNAME.github.io    |

Replace `YOUR-USERNAME` with your actual GitHub username.

**Option B — If using www subdomain (www.cophiaproperties.com):**

| Type  | Name | Value                      |
|-------|------|----------------------------|
| CNAME | www  | YOUR-USERNAME.github.io    |

> **Note:** DNS changes can take up to 24-48 hours to propagate, though it's usually much faster.

## Step 5: Add Your Photos

Create an `images` folder in your repo with subfolders:

```
images/
├── about-photo.jpg
├── ltr/
│   ├── property-1.jpg
│   ├── property-2.jpg
│   ├── property-3.jpg
│   └── property-4.jpg
├── str/
│   ├── property-1.jpg
│   ├── property-2.jpg
│   ├── property-3.jpg
│   └── property-4.jpg
└── remodel/
    ├── project-1-before.jpg
    ├── project-1-after.jpg
    ├── project-2-before.jpg
    ├── project-2-after.jpg
    ├── project-3-before.jpg
    └── project-3-after.jpg
```

Then update the `index.html` file — look for the HTML comments that say `<!-- Replace with: ... -->` and swap in `<img>` tags pointing to your image files.

## Step 6: Update Property Details

In `index.html`, search for and update:
- **LTR section**: Change "City, State" to actual city names, update property titles
- **STR section**: Add real addresses and replace `href="#"` with your Airbnb listing URLs
- **Remodel section**: Update project titles and descriptions
- **Contact form**: The form currently points to Formspree — sign up free at formspree.io and replace `YOUR_FORM_ID`

## Need Help?

Email Katie at katie@cophiaproperties.com
