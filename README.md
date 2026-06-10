# McEvoy Racing — Website Deployment Guide

---

## What is in this folder

```
mcevoy-racing/
├── index.html              ← The homepage
├── css/main.css            ← All the styling
├── js/main.js              ← All the functionality
├── netlify.toml            ← Netlify settings (don't touch)
├── admin/
│   ├── index.html          ← The CMS login page
│   └── config.yml          ← CMS field definitions (don't touch)
├── images/
│   ├── horses/             ← Horse photos go here
│   ├── news/               ← News article photos go here
│   ├── team/               ← Staff photos go here
│   └── facilities/         ← Facility photos go here
└── content/
    ├── horses/             ← Horse listing data
    ├── news/               ← News articles
    ├── results/            ← Race results
    ├── team/               ← Team member bios
    ├── facilities/         ← Facility descriptions
    └── settings/           ← Contact details, hero video URL
```

---

## Step 1 — Deploy to Netlify (one time only, 10 minutes)

1. Go to **netlify.com** and create a free account
2. Click **"Add new site"** then **"Deploy manually"**
3. Drag this entire `mcevoy-racing` folder onto the page
4. Your site will be live at a URL like `mcevoy-racing-xyz.netlify.app`

---

## Step 2 — Connect your domain (once you have one)

1. In Netlify go to **Site Settings → Domain Management**
2. Click **"Add custom domain"** and enter your domain name
3. Netlify will show you nameserver addresses
4. Go to wherever you bought your domain and point the nameservers to Netlify's
5. Takes 10-30 minutes to go live

---

## Step 3 — Enable logins for stable staff (one time only)

1. In Netlify go to **Site Settings → Identity**
2. Click **"Enable Identity"**
3. Under **Registration** set to **"Invite only"** (important — so random people can't sign up)
4. Under **Services → Git Gateway** click **"Enable Git Gateway"**
5. Go to **Identity → Invite Users** and enter each staff member's email
6. They will get an email to set their password
7. They log in at `yoursite.com.au/admin`

---

## Step 4 — Add the hero video

1. Upload your video to **Vimeo** (vimeo.com)
2. In Vimeo go to the video → **Settings → Privacy → Hide from Vimeo**
3. Click **Share → Embed** and copy the embed URL
4. Log into the site admin at `yoursite.com.au/admin`
5. Go to **Site Settings → Hero Video**
6. Paste the URL and click Save

---

## How stable staff update the site

### Adding a new horse
1. Go to `yoursite.com.au/admin`
2. Click **Horses → New Horse**
3. Fill in the form (lot number, breeding, price, spots available etc.)
4. Upload a photo and Tony's audio note if you have them
5. Click **Publish**
6. Done — the horse appears on the site within 30 seconds

### Updating shares sold
1. Go to **Horses** in the admin
2. Click the horse
3. Update the **"Shares Already Taken"** number
4. Click **Save** — the availability bar on the site updates automatically

### Adding a news article
1. Go to **News and Results → New Article**
2. Fill in the title, date, category, photo and text
3. Click **Publish**

### Updating race results
1. Go to **Race Results → New Result**
2. Fill in the horse, race, date, finishing position
3. Click **Publish**

### Updating team member bios or photos
1. Go to **Team Members**
2. Click the person
3. Update their photo or bio
4. Click **Save**

### Changing contact details or social links
1. Go to **Site Settings → Contact Details**
2. Update whatever has changed
3. Click **Save**

---

## Updating the video

If you need to change the hero video:
1. Upload the new video to Vimeo
2. Go to **Site Settings → Hero Video** in the admin
3. Paste the new embed URL
4. Save

---

## If something looks wrong

The site is very hard to break through the admin. If something looks off:
- Check that the content is marked as **Published** (toggle in each item)
- Make sure photos are uploaded (not just named)
- If in doubt, contact your developer — changes can always be undone

---

## Monthly costs

| Thing | Cost |
|---|---|
| Netlify hosting | Free |
| Domain (.com.au) | ~$20/year |
| Vimeo (no branding) | $20/month — optional |
| **Total minimum** | **~$2/month** |

---

## One line to change when you have your domain

In `netlify.toml` update the domain once it is confirmed.
Everything else is already configured.
