# chadtopaz.com — Static Site

## Before deploying

1. Drop these two image files into the `images/` folder:
   - `book-cover.jpg` (the Unlocking Justice cover)
   - `headshot.jpg` (the professional headshot)

## File structure

```
site/
  index.html              ← Homepage
  css/style.css           ← Shared stylesheet (all pages use this)
  images/                 ← Drop book-cover.jpg and headshot.jpg here
  about/index.html        ← Biography page
  book/index.html         ← Unlocking Justice page
  research/
    index.html            ← Publications (102 papers, auto-generated from spreadsheet)
    talks.html            ← Talks (214 talks, auto-generated from spreadsheet)
  speaking/index.html     ← Speaking & testimonials
  press/
    index.html            ← Op-eds
    coverage.html         ← Media coverage by topic
  music/index.html        ← Music / viola
  tda/index.html          ← Getting Started with TDA
```

## Deploying to Netlify

1. Go to netlify.com and sign up (use "Log in with GitHub")
2. Click "Add new site" → "Deploy manually"
3. Drag the entire `site/` folder onto the Netlify deploy area
4. Netlify gives you a URL like `random-name.netlify.app`
5. Go to Site Settings → Domain Management → Add custom domain
6. Type `chadtopaz.com`
7. Netlify shows you DNS records to add — go to your domain registrar and update them
8. Done — usually propagates within an hour

## Updating content

When you need to update something (new paper, new talk, content change):
- Tell Claude what to change
- Claude edits the relevant HTML file
- You download the updated file and re-drag the `site/` folder to Netlify
  (or connect GitHub for automatic deploys)

## Updating publications/talks from spreadsheet

The publications and talks pages are generated from your Academic_Tracking.xlsx spreadsheet.
When you have new papers or talks to add:
1. Update the spreadsheet
2. Tell Claude to regenerate research/index.html and/or research/talks.html
3. Deploy the updated files

