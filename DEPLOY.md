# Abdurazaq Gorja portfolio: going live on zaqmedia.film

This folder is the whole website. There is no build step: `index.html` plus the `media` folder.

## 1. Let Vimeo play on your site (about 5 minutes)

Do this for every video on the site:

1. Open the video on vimeo.com and go to **Settings → Privacy**.
2. Under **Where can this be embedded?**, choose **Specific domains**.
3. Add `zaqmedia.film` and `www.zaqmedia.film`. If you test on Netlify first, also add your `*.netlify.app` address.
4. Save.

If a video still won't play, check that its **Who can watch** setting is not "Only me". Public, unlisted and "hide from Vimeo" all work.

## 2. Put the site online (Netlify, free)

1. Go to https://app.netlify.com/drop and sign in (or create a free account).
2. Drag the whole `zaqmedia-site` folder onto the page.
3. Netlify gives you a test address such as `zaq-media.netlify.app`. Open it and check that the videos play.

## 3. Connect zaqmedia.film

1. In Netlify, open the site and go to **Domain management → Add a domain**, then enter `zaqmedia.film`.
2. Netlify shows the DNS records to add. Add them where you bought the domain:
   - `A` record for `@` pointing to Netlify's load balancer IP (Netlify shows the current one)
   - `CNAME` record for `www` pointing to your `*.netlify.app` address
3. Wait for DNS to update (minutes to a few hours). Netlify turns on HTTPS automatically.

## Updating the site later

- **Replace a video:** in `index.html`, find the project in the `const all = [ ... ]` list and change its Vimeo `id`.
- **Add a video:** add a line to that list (`img` is the still in `media/`, `id` is the Vimeo number), then add its `img` name to a project's `shots` list in `const projects`.
- **Republish:** drag the folder onto Netlify again (Deploys → drag and drop).
