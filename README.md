# Bubu's Kitchen ♥

A cooking app made with love for Bubu. Cook mode, timers, editable recipes, stainless-steel notes.

Offline-capable recipe app for cooking on an iPad: cook mode, timers, editable recipes and stainless steel pan guidance.

Open the GitHub Pages address in Safari, tap Share, then Add to Home Screen.

## Sync between two devices (optional, free)

Shares day plans, new/edited recipes and per-person favourites (shown as ♥ Name). Uses a Firebase Realtime Database you own.

1. Go to https://console.firebase.google.com and create a project (no Analytics needed).
2. Build → **Realtime Database** → Create database (any region) → start in locked mode.
3. Open the **Rules** tab, paste this and **Publish**:
   ```json
   {"rules":{"rooms":{"$room":{".read":true,".write":true}}}}
   ```
   Only someone who knows the long shared code can read or write a room.
4. Copy the database URL (ends in `firebasedatabase.app`).
5. In the app tap **Sync**, paste the URL, tap **Make a code**, enter your name, **Connect**.
6. Tap **Sync → Copy invite link**, send it to your partner, open it on their iPad, enter their name, **Connect**.

Deleting a recipe is not synced. Plans and recipe edits use last-change-wins.
