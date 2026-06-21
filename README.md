# KPW Photo Curator

Internal tool for reviewing and approving client photos before they go into Agency Brain content generation.

**Live URL:** https://bbotai.github.io/kpw-photo-curator

---

## How to Find Your Cloudinary API Key and Secret

1. Log in at [cloudinary.com](https://cloudinary.com)
2. Go to **Settings → API Keys**
3. Copy your **API Key** and **API Secret**

These are entered in the browser prompt each session — they are never stored beyond the current tab.

---

## How to Use

1. Open **bbotai.github.io/kpw-photo-curator**
2. Type the client folder name (e.g. `mikes-services-llc`) — same slug used on the upload page
3. Click **Load Photos**
4. Enter your Cloudinary **API Key** and **API Secret** when prompted
5. Click photos to cycle their status:
   - ⬜ **Unreviewed** (default)
   - ✅ **Approved** (green border) — will be used in content
   - ⏭ **Skip** (red, dimmed) — excluded
   - Back to ⬜ Unreviewed
6. **Double-click** any photo to mark it as ⭐ **Story Set** (gold border)
   - Story Sets are groups of related photos for carousel or multi-image posts
   - Story Set photos are also included in the approved pool
7. Review the live count in the bottom bar: **X approved · Y story set · Z skipped**
8. Click **Save to Agency Brain** when done

Photos saved to Agency Brain will be used automatically the next time content is generated for that client — real photos rotate in before any AI-generated images.

---

## What "Save to Agency Brain" Does

- Sends all Approved + Story Set photo URLs to the Agency Brain spreadsheet
- Populates the **Image Library URLs** column for the matching client row
- Saves Story Set groupings to the **Story Sets** column
- Next content generation run will pull unused photos first, rotating through the library over time

---

## GitHub Pages Setup

1. Go to [github.com/BbotAI/kpw-photo-curator](https://github.com/BbotAI/kpw-photo-curator)
2. Click **Settings → Pages**
3. Under **Branch**, select `main` and `/ (root)`
4. Click **Save**

Live in ~60 seconds.
