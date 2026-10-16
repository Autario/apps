# autario apps

Open-source data apps that run on [autario](https://autario.com). Each app is a single HTML file that reads your connected data through `autario.js`. Fork one, paste it into autario, and it runs on your own data in a minute.

## Run an app on your data

1. Open the app folder below and copy `index.html`.
2. Sign in at [autario.com/developer/build](https://autario.com/developer/build), choose **Paste HTML**, paste, pick the datasets the app may read, click **Run it**.
3. The app runs in a sandbox on autario, refreshes with your connectors, and you can share it with a link.

No build step, no hosting, no API keys in the file.

## Apps

| App | What it shows | Data it reads |
|---|---|---|
| [instagram-followers](apps/instagram-followers) | Followers, reach, posts, reels, stories, best hours and demographics for one Instagram account | Instagram Insights connector |
| [top-rows](apps/top-rows) | The first rows of any dataset you connected, as a table | any dataset you pick |

## How an app talks to autario

`autario.js` is injected into every app autario serves. The whole API:

```js
const { app, user } = await autario.ready();         // app name, viewer role
const list = await autario.datasets();                 // datasets this app may read
const rows = await autario.query(list[0].id, { limit: 100, orderBy: 'date desc' });
await autario.artifacts.set('view', { metric: 'clicks' }); // saved per app (editor or higher)
```

Docs: [autario.com/developer/docs/autario-js](https://autario.com/developer/docs/autario-js)

## Contribute an app

See [CONTRIBUTING.md](CONTRIBUTING.md). Short version: one folder, one `index.html`, one `README.md`, one screenshot, no external network, data only through `autario.js`. Open a pull request.

## License

MIT. Use the apps however you like, on autario or elsewhere.
