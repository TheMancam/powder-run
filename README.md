# Powder Run

Low-poly 3D downhill ski game, packaged as an Android app.

Every push to `main` builds the app on GitHub Actions. When the build finishes, open the repo's **Releases** page, download `powder-run.apk` from the **latest** release and install it.

The workflow file lives at `.github/workflows/build-apk.yml` (a copy is also kept at the top level as `build-apk.yml`). Files are kept flat so they can be uploaded from a phone; the workflow arranges them into a Capacitor project before building.

Builds are signed with the debug key in `debug.keystore`, so a new build installs over the old one. That key is for personal builds only, not for the Play Store.
