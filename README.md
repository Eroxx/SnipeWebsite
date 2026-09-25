# Snipe — the public site

Source of truth for <https://eroxx.github.io/SnipeWebsite/>.

This folder lives in the **app** repo on purpose, the same way Crate's does: a feature and
the page claiming it can then change in one commit, which is how the site stopped naming
things the app no longer did. `publish.sh` copies it to `Eroxx/SnipeWebsite`, which GitHub
Pages serves. Editing that repo directly will be overwritten on the next publish.

```
./publish.sh "what changed"
```

| file | |
|---|---|
| `index.html` | the whole marketing page: markup, styles, one reveal script |
| `privacy.html` | required by App Store Connect, linked from the app's Settings |
| `support.html` | same, and the answers to the questions the app actually raises |
| `assets/` | screenshots, icon, favicons, social card |

Screenshots are rendered from the real `snipe.html` against the real watchlist, in the
app's dark palette, at true device sizes at 2x. They are not mockups and the page says so,
so re-shoot them rather than editing them.
