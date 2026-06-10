# TreasureX Landing Page

Beautiful landing page for treasurex.app

## Features

✨ **Premium Design**
- Violet theme matching your app
- Smooth animations
- Mobile responsive
- Email signup form

📧 **Email Collection**
- Collects emails for launch notification
- Success confirmation
- Ready to integrate with backend

🎨 **Sections**
- Hero with email signup
- Features grid (6 features)
- Stats showcase
- App store badges (coming soon)
- Social links footer

## Quick Deploy to Vercel (EASIEST - 5 Minutes)

### Step 1: Push to GitHub

1. **Create new GitHub repo:**
   - Go to https://github.com/new
   - Name: `treasurex-landing`
   - Public repo
   - Don't initialize with README

2. **Push this folder:**
   ```bash
   cd landing-page
   git init
   git add .
   git commit -m "Initial landing page"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/treasurex-landing.git
   git push -u origin main
   ```

### Step 2: Deploy to Vercel

1. **Go to:** https://vercel.com/signup
2. **Sign up** with GitHub
3. **Click** "New Project"
4. **Import** your `treasurex-landing` repo
5. **Deploy** (no config needed!)
6. **Done!** You'll get a URL like: `treasurex-landing.vercel.app`

### Step 3: Connect Custom Domain (treasurex.app)

**In Vercel Dashboard:**

1. Click your project
2. Go to **Settings** → **Domains**
3. Add domain: `treasurex.app`
4. Vercel will show you DNS records

**You'll need to add in GoDaddy:**
```
Type: A
Name: @
Value: 76.76.21.21

Type: CNAME
Name: www
Value: cname.vercel-dns.com
```

**In GoDaddy:**
1. Go to **My Products** → **Domains**
2. Click **treasurex.app**
3. Click **DNS** → **Manage DNS**
4. Add the records Vercel gave you
5. Wait 5-60 minutes for DNS propagation

**DONE!** Your site will be live at https://treasurex.app

---

## Alternative: Deploy to Netlify

### Step 1: Create Netlify Account

1. Go to https://netlify.com
2. Sign up with GitHub
3. Click **Add new site** → **Import existing project**
4. Choose your GitHub repo
5. Deploy!

### Step 2: Add Custom Domain

1. In Netlify: **Domain Settings**
2. Add `treasurex.app`
3. Follow DNS instructions (similar to Vercel)

---

## Customize Your Landing Page

### Change Colors

Edit `index.html` - find these CSS variables:

```css
/* Main violet: #7C3AED */
/* Dark violet: #6D28D9 */
/* Light violet: #A78BFA */
```

### Update Content

1. **Hero Title:** Line 187
2. **Features:** Lines 219-254
3. **Email Form:** Line 196
4. **Social Links:** Lines 310-312

### Add Email Collection Service

Replace line 344 with your email service:

**Option A: Mailchimp**
```javascript
fetch('https://YOUR_MAILCHIMP_URL', {
    method: 'POST',
    body: JSON.stringify({ email })
});
```

**Option B: ConvertKit**
```javascript
fetch('https://api.convertkit.com/v3/forms/YOUR_FORM_ID/subscribe', {
    method: 'POST',
    body: JSON.stringify({ email, api_key: 'YOUR_API_KEY' })
});
```

**Option C: Supabase (Your existing DB)**
```javascript
fetch('https://YOUR_PROJECT.supabase.co/rest/v1/email_signups', {
    method: 'POST',
    headers: {
        'apikey': 'YOUR_ANON_KEY',
        'Content-Type': 'application/json'
    },
    body: JSON.stringify({ email })
});
```

---

## What's Included

- ✅ Mobile responsive
- ✅ Fast loading
- ✅ SEO optimized
- ✅ Email signup
- ✅ Social links
- ✅ App store badges
- ✅ Premium animations
- ✅ Violet theme
- ✅ No dependencies (pure HTML/CSS/JS)

---

## Need Help?

1. **Can't push to GitHub?** Let me know
2. **DNS not working?** It takes 5-60 minutes
3. **Want to customize?** I can help edit anything
4. **Email collection not working?** I'll set up Supabase endpoint

---

## Next Steps

After deployment:

1. ✅ Test on mobile
2. ✅ Share on social media
3. ✅ Add to email signature
4. ✅ Use in marketing materials
5. ✅ Track email signups
