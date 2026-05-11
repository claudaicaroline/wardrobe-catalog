# Adding more photos to your wardrobe catalog

## How the folder is organized

```
Wardrobe/
  wardrobe.html        ← open this in your browser to view the dashboard
  catalog.json         ← the database of items and their tags
  photos/              ← full-size JPEGs (used in the detail modal)
  thumbs/              ← small JPEGs (used in the grid)
  HOW_TO_ADD_MORE_PHOTOS.md  ← this file
```

## To add more photos

1. **Photograph the items** (no need to iron, just like before — the catalog is for you, not Vogue).
2. **Drop the new photos** into a dated folder inside `Creative stuff/`, just like the `10 May 2026` folder. HEIC, JPG, or PNG all work.
3. **Ask me in the next conversation:** "I added new photos in [folder name], please add them to the wardrobe catalog."

I'll then:
- Convert any HEIC files to JPEG
- Generate thumbnails
- Auto-tag each new item
- Detect front/back pairs
- Append them to `catalog.json`
- Refresh the dashboard

## Saving and exporting your edits

Every change is saved instantly to your browser's localStorage — that means edits, notes, statuses, hidden items, and saved outfits all persist between browser sessions automatically. You don't need to click anything extra after Save.

For stronger durability (across browsers, computers, or browser-data resets), use one of these:

### Option 1 (recommended): Sync to file

Click **🔗 Sync to file** in the toolbar. The browser will ask where to save `wardrobe-edits.json` — pick the Wardrobe folder. From that point on, every save also writes to that file automatically. The next time you open the dashboard the file gets read back in, even if your browser data was cleared.

This needs Chrome or Edge (the File System Access API isn't in Safari or Firefox yet). Each browser session may ask for permission once via a "Reconnect" banner.

### Option 2: Manual export/import

- Click **Export edits** to download a snapshot JSON anytime.
- On a new browser or computer, click **Import edits** and pick the JSON.

Use this if you're on Safari/Firefox, or just want a periodic backup.

## Quick reminders about the current catalog

- **IMG_1964** is flagged for review — it looks like a screenshot/selfie rather than a clothing item. Open it in the dashboard and either correct the type or skip it.
- A few items were detected as front/back pairs (denim vest, camel "QUEEN" shirtdress, the burgundy floral dress, etc.). Use the **Hide back-of-item shots** toggle to declutter the grid; the back view is still linked from each item's detail modal.
- **IMG_2048** — I wasn't sure if this is a third view of the cream linen top with belt, or a separate item. Worth a quick confirm.
- All my auto-tags are best-guess. Click any item to correct type, season, occasion, source, or status, and add personal notes.

## Tips for getting the most out of the dashboard

- Use the **Status** filter (keep / unsure / donate / favorite) once you start a declutter pass. Favorites get a gold star instead of a colored dot.
- The **Source** field is empty by default — fill it in as you remember where things came from. Filtering by `thrifted` later is a fun way to see your treasure-hunting history.
- **Auto-detected fields** (pattern, sleeves, length, neckline) are now editable dropdowns inside the modal. Set anything wrong to "— none —" to remove it (handy for skirts that got tagged with sleeves).
- **Hide from wardrobe** removes an item from the grid without deleting the photo. Use "Show hidden items" in the toolbar to see them again.
- **Linked outfits** show up in the modal of any item that's part of a saved outfit — click to jump to that outfit.
- The **Outfit planner** is on-demand: click items to add them, name the outfit, save. Edit or delete saved outfits from the panel.
- Search works across types, colors, patterns, notes, and your custom tags.

## Color palette

Colors are normalized to a small set so filtering stays useful. Behind the scenes:
- olive, sage → **green**
- dark grey, light grey, charcoal, silver → **grey**
- tan, camel, taupe, khaki, champagne → **beige** (champagne is **cream**)
- light blue, denim blue → **blue**; dark blue → **navy**
- wine → **burgundy**; coral → **orange**

You can always override individual items in the modal if you disagree with a normalization.
