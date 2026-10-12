# Memories: Re-Live website

Static marketing, privacy and support pages for the iPhone/iPad app. No build step, JavaScript tracking, external fonts or third-party video embeds.

## Files

- `index.html`: landing page, app features and the approved 16-second simulated-feed marketing demonstration.
- `privacy.html`: policy matching current local iOS storage, permissions, backups, Apple services and public support data.
- `support.html`: getting started, troubleshooting and links to GitHub Issues.
- `styles.css`: responsive light/dark styles, keyboard focus and reduced-motion support.
- `assets/`: app icon, demonstration video and poster; owner-authorized sample media.
- `.github/ISSUE_TEMPLATE/`: public support and privacy-question forms.
- `.nojekyll`: serve these static files directly with GitHub Pages.

No app source, signing material, private phone media or account credentials belong here.

## Preview locally

From this folder:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000/ in your browser. Press Control+C to stop.

## Publish in order

1. Review the privacy/support wording and commercial rights for the supplied marketing assets.
2. Commit the website files and push to the website repository:

```sh
git status --short
git diff --check
git add index.html privacy.html support.html 404.html styles.css assets .github .gitignore .nojekyll README.md
git diff --cached --stat
git commit -m "Add Memories Re-Live marketing, privacy and support pages"
git push origin main
```

3. Open this repository's **Settings → Pages**. Choose **Deploy from a branch**, branch **main**, folder **/ (root)**, and Save. Repository visibility/plan must permit GitHub Pages.
4. Wait for the Pages deployment to finish. Open all three URLs below in a signed-out browser; they must load publicly over HTTPS. Enable **Enforce HTTPS** if the setting is available. Confirm Issues is enabled under repository Settings → General → Features.
5. In App Store Connect, paste the corresponding URLs into **Privacy Policy URL**, **Support URL** and optional **Marketing URL**.
6. Ensure the app itself includes an accessible privacy-policy link before submission, and keep App Privacy answers consistent with the release build. The app code was not modified by creating this website.

After deployment, expected URLs:

| App Store field | URL |
| --- | --- |
| Privacy Policy URL | https://datta-lohith.github.io/memories-website/privacy.html |
| Support URL | https://datta-lohith.github.io/memories-website/support.html |
| Marketing URL (optional) | https://datta-lohith.github.io/memories-website/ |

These URLs are publishing targets, not a claim that deployment has occurred. Update canonical links and issue-template contact links if you later change the domain.

[GitHub Pages publishing instructions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) · [Apple App Privacy instructions](https://developer.apple.com/help/app-store-connect/manage-app-information/manage-app-privacy/)

## Maintenance

Update the policy whenever app data practices change. Revise the effective date when its substance changes. The current policy covers iOS; audit Android before using it for a Google Play release. When the app is publicly available, replace “release coming soon” with the verified App Store link.

The demonstration is explicitly labeled simulated camera footage; it is for this marketing site, not certification of App Store App Preview eligibility. Source: owner-created dog/camera clips, composited and captured in an isolated simulator. The app icon is copied from the owner's app. No production camera behavior is changed.

Public GitHub Issues is the owner-selected contact channel. Reports are visible to everyone; do not solicit private media, identifying information or credentials. Do not promise private support or guaranteed response times.

## Daily changes

### 2026-10-11

- Created landing, privacy and support pages, responsive theme, public issue forms and static hosting configuration. Added approved sample demonstration and app icon.
- Documented local preview and ordered GitHub Pages/App Store Connect setup. HTML nesting/local links checked; all pages and assets served HTTP 200 locally; approved video integrity verified. Files are prepared locally; no commit, push or publishing has been performed.
