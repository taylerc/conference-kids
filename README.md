# Conference Kids

Bingo, notes and a points-for-rewards system to help kids follow General Conference.
One static page with no server, no accounts and no build step.

## Put it on GitHub Pages

1. On github.com, click **New repository**, name it `conference-kids`, make it **Public**, and create it.
2. On the new repo page, click **uploading an existing file** and drag in
   `index.html`, `manifest.json`, `icon.svg` and this README. Click **Commit changes**.
3. Go to **Settings → Pages**. Under *Branch*, choose `main` and `/ (root)`, then **Save**.
4. After a minute the site is live at `https://<your-username>.github.io/conference-kids/`.

## Set up your family (parents, once)

1. On your own phone or computer, open the site and tap **Create our family**.
2. Choose a parent code (any code or password, 4+ characters). It works on every device.
3. In **⚙️ Parents**, tap **＋ Add a kid** for each child (first names only).
4. Under **Invite links**, tap **🔗 Share** next to each child and send it to their tablet.

## Put it on each tablet

Open the child's link on their tablet, then:
- **iPad:** Share button → **Add to Home Screen**
- **Android:** browser menu (⋮) → **Add to Home screen** / **Install app**

It opens straight to that child's screen, full-screen like an app.

## How it works

- **Live sync:** points, bingo cards, notes and drawings are saved in a Firebase Realtime
  Database and update on every device within a second. A family scoreboard shows on each
  child's screen.
- **Bingo:** five boards (Word Hunt, Look & See, Stories & Moments, Little Kids, Mix-It-Up).
  Every card is shuffled. Each completed line = 10 points, full card = 50 bonus.
  Unmarking a square takes those points back, so tapping on and off earns nothing.
- **Notes:** type, tap sentence starters, or draw. Tagged by session.
- **Rewards:** parents set prizes and costs. Redeeming needs the parent code.
- **Parents (⚙️):** add and edit kids, share links, adjust points, add rewards, change point
  values, change the code, reset for next conference, see recent activity.

## Good to know

- **The link is the key.** There are no logins. Anyone with a family link can open that family,
  so only send links to your kids. Database rules stop anyone from listing or finding families.
- The parent code keeps kids out of the parent screen. It is not strong security against
  someone tech-savvy who has the link.
- Without internet, changes are kept on the device and sync when it reconnects.
- **Erase family** (in ⚙️ Parents) deletes everything on every device and stops the links working.
- Firebase project: `conference-kids` (console.firebase.google.com). Free Spark plan.
- To change bingo squares, edit the `WORDS`, `LOOK`, `STORIES` and `LITTLE` lists near the
  top of the `<script>` in `index.html`. Each square is `{t:"Text", e:"emoji"}`.
