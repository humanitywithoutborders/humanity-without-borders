# HWB administration — setup required

The files `admin/index.html` and `admin/config.yml` install the Decap CMS interface, **not working authentication**. GitHub Pages cannot run an OAuth server. Before `/admin/` can log in, configure a trusted GitHub OAuth bridge/service and register a GitHub OAuth application; add the bridge `base_url` and any required `auth_endpoint` to `admin/config.yml`. Never commit a GitHub access token, OAuth client secret, or private key to this public repository. Only authorize your own GitHub account and limit permissions to this repository where supported.

Decap currently edits the **English-source homepage** fields in `content/home.json`; the homepage reads this JSON on load. Existing `i18n.js` translates recognized English strings, but new/changed copy will require explicit Persian and Arabic translations to avoid untranslated text. The remaining pages are still controlled by `app.js`; they are not yet CMS-editable. Donation and contact buttons remain nonfunctional placeholders. Do not represent them as live services.

## Publish

Upload the **contents** of this project to the root of your GitHub repository (not the containing folder), keeping directories `admin/` and `content/` intact. Use a test branch or repository first and back up your existing site. Verify the public site works before attempting OAuth setup.

## Important

The admin URL is `https://humanitywithoutborders.github.io/humanity-without-borders/admin/` only after publishing these files. It is publicly reachable, but publishing permissions are controlled by GitHub authentication. A working login requires the separate OAuth configuration described above.
