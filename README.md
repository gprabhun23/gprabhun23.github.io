# Spot & Steer AR developer website

A small static site for GitHub Pages:

- `index.html`: the game's page, with a link to its Google Play listing.
- `privacy-policy.html`: the privacy policy. Use its URL in the Play listing.
- `app-ads.txt`: the AdMob seller line. AdMob only reads it at the **root** of your website.
- `style.css`, `images/`, and `fonts/` (Outfit, SIL Open Font License; licence included).
- `.nojekyll`: tells GitHub Pages to serve the files exactly as they are.

## Why it must be the `<username>.github.io` repository

AdMob looks for the file at `https://<your website>/app-ads.txt`, at the root of the domain, and nowhere else. On GitHub
Pages only a repository named exactly **`<username>.github.io`** is served at the root:
`https://gprabhun23.github.io/app-ads.txt`. Any other repository is served under a folder
(`https://gprabhun23.github.io/SomeRepo/`), and AdMob won't find `app-ads.txt` there.

## Publish (about 5 minutes)

1. On github.com, create a **New repository** named exactly `gprabhun23.github.io`. Make it **Public**. Leave "Add a README" unticked.
2. Put the contents of this `Website` folder into it, with `app-ads.txt` at the top level, not inside a folder. Either:
   - on the repository page, choose **Add file > Upload files** and drag in everything inside `Website/` (including the `images` and `fonts` folders), then **Commit**; or
   - push them with git.
3. Open **Settings > Pages** and set Source to **Deploy from a branch**, Branch **main**, folder **/ (root)**.
4. After a minute, check that `https://gprabhun23.github.io/app-ads.txt` shows the single `google.com, pub-…` line.

## Then tell Google Play and AdMob

1. **Play Console:** open **Grow users > Store presence > Store settings > Store listing contact details > Website**, enter `https://gprabhun23.github.io`, and save.
   - It must be exactly this root address, with no path.
   - If your Play listing doesn't have a privacy policy link yet, use `https://gprabhun23.github.io/privacy-policy.html` (**App content > Privacy policy**).
2. **AdMob:** open **Apps > app-ads.txt** and use **Check for updates**. AdMob crawls within about 24 hours, and the status turns to "Authorized" once it matches.
