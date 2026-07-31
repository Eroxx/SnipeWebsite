# Snipe — marketing site

The public site for **Snipe**, an App Store price watcher for macOS, iPhone and iPad.
The app itself lives in a separate private repo.

A single static page. No build step, no dependencies — open `index.html` and it works.
GitHub Pages serves it from `main` at the repository root; `.nojekyll` stops Jekyll from
touching it.

```
index.html    the whole site: markup, styles and one small reveal script
assets/       screenshots, app icon, favicons, social card
```

## Screenshots

`assets/iphone-onsale.png` and `assets/ipad-inspector.png` are real captures from the
iOS Simulator, taken with a clean marketing status bar:

```
xcrun simctl status_bar <udid> override --time "9:41" --batteryState charged \
  --batteryLevel 100 --cellularMode active --cellularBars 4 --wifiBars 3
```

## Local preview

```
python3 -m http.server 8731
```

## Honesty notes

The app is not on the App Store yet, so the page says **Coming soon** rather than linking
to a store page. When it ships, replace the `.btn.primary` span in `index.html` with a real
link. Nothing on this page claims a rating, a review or a download count.
