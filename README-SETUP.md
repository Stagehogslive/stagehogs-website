# The StageHogs — Launch Kit v2

This package preserves the approved custom HTML design and adds:
- Featured YouTube video and two secondary videos
- “All Killer. No Filler.” headline and updated band story
- Data-driven upcoming shows (content/shows.json)
- Data-driven photo gallery (content/gallery.json)
- Decap CMS editor configuration at /admin/

## Preview
For a local preview, run `python3 -m http.server 8000` inside this folder and open http://localhost:8000. Opening index.html directly from disk can prevent JSON data from loading due to browser file security rules.

## Publish
1. Create a GitHub repository and upload the entire folder (index.html at repo root).
2. Connect the GitHub repository to Netlify and publish as a static site (no build command; publish directory `.`).
3. Replace `YOUR_GITHUB_USERNAME/YOUR_REPOSITORY` in admin/config.yml with the actual repository name.
4. Configure GitHub OAuth for Decap CMS using a compatible authentication gateway/proxy. Netlify hosting alone does **not** provide Decap GitHub OAuth or an admin login automatically. This is an additional setup step; /admin/ will not work until authentication is configured.
5. Test the admin login, publishing a new show, uploading a photo, and automatic Netlify deployment.
6. Connect a custom domain after purchase and configure HTTPS/DNS.

## Editing before CMS authentication is configured
Edit content/shows.json and content/gallery.json directly in GitHub, commit changes, and Netlify will redeploy. Dates use YYYY-MM-DD. The site automatically hides past shows based on Pacific time.

## Booking / EPK
The booking link currently uses the band's Facebook page. A direct booking email and downloadable EPK are pending final contact and technical details. The complete 36-song repertoire is not published here yet; it can be added to the EPK once confirmed.

## Important
YouTube playback requires an internet connection and the video owner's embedding permission. Local file previews may not show data-driven shows/photos; use a local web server.
