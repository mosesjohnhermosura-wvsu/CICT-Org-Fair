# CICT Org Fair

**Live site:** https://mosesjohnhermosura-wvsu.github.io/CICT-Org-Fair/

A Flutter app for the CICT Org Fair. Browse orgs, see what's on, join an org
and view your schedule. Events are published in Contentful (a headless CMS)
and the app reads them through its Content Delivery API, so officers can
change events without a new release.

## Run it locally

1. Copy `cms.example.json` to `cms.json` and fill in your Contentful values.
   `cms.json` is in `.gitignore` and is never committed.
2. `flutter pub get`
3. `flutter run -d chrome --dart-define-from-file=cms.json`

## Tests

`flutter analyze` and `flutter test`. GitHub Actions runs both on every pull
request and push (`.github/workflows/ci.yml`). Every push to `main` that passes
the tests is deployed to GitHub Pages (`.github/workflows/deploy.yml`).
