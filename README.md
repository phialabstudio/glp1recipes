[README-USER.md](https://github.com/user-attachments/files/29281972/README-USER.md)
# Phia Fridge Cookbook — Simple Deploy Guide (no coding)

The plain-English version. Just follow the steps.

## What you're putting live
A free recipe web app at **recipes.phialabstudio.com** that people can install on their phone like a real app (with your plate icon). Email is captured by your GHL opt-in *before* this page; this page nudges people toward your $17 tracker.

## What's in this folder
Upload **ALL of these together** — they only work as a set:
- `index.html` — the cookbook page (the main one)
- `manifest.json` + `sw.js` — what makes it installable
- `phia-icon-*.png` + `favicon.ico` — your app icon
- `phia-icon.svg` — the editable icon (you don't upload this one, just keep it)

⚠️ Don't upload only `index.html`. It needs the other files sitting next to it, or the app icon and install won't work.

## How to put it live (GitHub — your method)
1. Go to **github.com** and open your cookbook repository (the one linked to Vercel).
2. Click **Add file → Upload files**.
3. Drag in **all the files** from this folder at once. *(GitHub lets you select many at once — that's the trick vs Vercel Drop, which took one at a time.)*
4. Scroll down, type a short note like `add app icon + PWA`, click **Commit changes**.
5. Vercel republishes automatically — wait about 1 minute.
6. Open **recipes.phialabstudio.com** and hard-refresh (hold **Shift** and click reload).

## Check it worked
On your phone, open **recipes.phialabstudio.com**:
- iPhone → **Safari** → Share → **Add to Home Screen**
- Android → **Chrome** → menu → **Add to Home Screen / Install**

Your plate icon should appear on the home screen. 🎉

## If you change recipes later
1. Re-upload the new `index.html` the same way.
2. **Important:** open `sw.js`, find `phia-cookbook-v1`, change it to `v2` (then `v3` next time…). Without this, people keep seeing the old cached version.
3. Commit. Done.

No terminal, no code — just upload and commit.
