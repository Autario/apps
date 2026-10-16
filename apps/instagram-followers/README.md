# Instagram dashboard

One page for an Instagram account: followers, views, interactions and link taps for the last 28 days, reach and new followers per day, every recent post and reel with engagement rate, reel watch time and skip rate, stories with navigation (where viewers dropped off), when your followers are online, and follower demographics by age, gender, country and city.

Built in one minute from a prompt, then pasted into autario. No library, no build step: plain SVG charts, sortable tables, and the metric picker remembers your last choice per app.

## Data it reads

The **Instagram Insights** connector on autario (connect it under Connectors, Instagram login is enough). Tick all its reports when you run the app; the app finds them by title:

- Account snapshot (followers, following, posts)
- Account totals (last 28 days)
- Account reach by day, Followers by day
- Views, reach and interactions by day
- Engaged accounts, story replies, reposts, follows and unfollows by day
- Recent posts with engagement, Follows and profile visits per post
- Reel watch time
- Stories, Story replies/follows/profile visits/link taps, Story navigation
- Followers online by hour
- Follower demographics (age, gender, country, city)

A report you did not tick, or that has not fetched yet, shows an honest empty state on its cards. Nothing else is needed.

## Run it

Copy `index.html`, open https://autario.com/developer/build, choose **Paste HTML**, paste, tick the Instagram Insights datasets, click **Run it**.
