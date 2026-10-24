# EraseLikedVideo_Youtube

A browser console script that removes every video from your YouTube "Liked videos" list.

## How to use
1. Open https://www.youtube.com/playlist?list=LL
2. Press F12 and open the **Console** tab
3. **First time only:** Chrome/Edge/Firefox block pasting into the console.
   Type `allow pasting` and press Enter.
4. Paste the contents of `erase-liked-videos.js` and press Enter
5. Keep the tab open and in the foreground until it prints `Done`
6. If videos are still left, refresh the page and run it again

## Stop early
Type this in the console:
    window.stopUnlike = true

## Notes
- YouTube stops loading new rows after a few hundred removals, so large lists need a few runs.
- If many items are skipped, raise `DELAY` in the script (e.g. 600).
- It works by clicking YouTube's own menus, so a YouTube layout change can break it.
