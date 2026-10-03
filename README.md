# Conference Kids

Bingo, notes and a points-for-rewards system to help kids follow General Conference.
One static page with no server, no accounts and no build step.

## Put it on GitHub Pages

1. On github.com, click **New repository**, name it `conference-kids`, make it **Public**, and create it.
2. On the new repo page, click **uploading an existing file** and drag in
   `index.html`, `manifest.json`, `icon.svg` and this README. Click **Commit changes**.
3. Go to **Settings → Pages**. Under *Branch*, choose `main` and `/ (root)`, then **Save**.
4. After a minute the site is live at `https://<your-username>.github.io/conference-kids/`.

## Put it on each tablet

Open that link on the tablet, then:
- **iPad:** Share button → **Add to Home Screen**
- **Android:** browser menu (⋮) → **Add to Home screen** / **Install app**

It then opens full-screen like an app.

## How it works

- **Kids:** each child adds themselves with a name, animal and color.
- **Bingo:** five boards (Word Hunt, Look & See, Stories & Moments, Little Kids, Mix-It-Up).
  Every card is shuffled. Each completed line = 10 points, full card = 50 bonus.
  Unmarking a square takes those points back, so tapping on and off earns nothing.
- **Notes:** type, tap sentence starters, or draw. Tagged by session.
- **Rewards:** parents set prizes and costs. Redeeming needs the parent code.
- **Parents (⚙️ on the home screen):** the first time, you create a parent code (any code or
  password, 4+ characters). After that it is required to get in. Adjust points, edit kids,
  add rewards, change point values, change the code, reset for next conference.

## Good to know

- Data is saved **on each device** (browser storage). Points earned on one tablet stay on
  that tablet. Clearing Safari/Chrome website data erases it.
- The parent code is per device too: set one on each tablet before handing it over.
  **Forgot the code?** On that tablet, clear the site's website data in browser settings.
  That also erases its points and notes.
- To change bingo squares, edit the `WORDS`, `LOOK`, `STORIES` and `LITTLE` lists near the
  top of the `<script>` in `index.html`. Each square is `{t:"Text", e:"emoji"}`.
