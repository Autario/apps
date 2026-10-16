# Contributing an app

One folder under `apps/`, named in kebab-case. Inside:

```
apps/<your-app>/
  index.html     the whole app, one file
  README.md      what it shows, which datasets it expects, one screenshot
  screenshot.png
```

## Rules

1. **One file.** Everything inline: HTML, CSS, JavaScript. autario serves the app in a sandbox that has no network, so a second file or a CDN script will not load.
2. **Data only through `autario.js`.** `autario.ready()`, `autario.datasets()`, `autario.query()`, `autario.artifacts`. No `fetch`, no `XMLHttpRequest`, no WebSocket, no `<script src>` other than `https://autario.com/autario.js`.
3. **No `eval`, no `new Function`, no string timers.** autario's content gate rejects them before publishing.
4. **No secrets, no personal data in the file.** The app sees only the datasets its owner declares.
5. **Scrolls like a document.** No fixed-height wrapper with its own scrollbar; the page may grow with its content.
6. **Say what data you expect.** In README.md, name the connector and columns the app reads (for example `instagram_insights.follower_demographics`, columns `city`, `followers`). A reader without that connector should understand what to connect.

## Test it before the pull request

1. Sign in at https://autario.com/developer/build, choose **Paste HTML**, paste your `index.html`, pick the datasets, click **Run it**.
2. The app must render with the datasets you named and show an honest empty state when a dataset is missing.
3. Take the screenshot from that run.

## Pull request

Fork, add your folder, open a pull request with the README text as description. Maintainers run the app once on their own data before merging.

By contributing you agree your app is published under the MIT license of this repository.
