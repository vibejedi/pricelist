# How to edit prices & laptops (Excel)

The website now has a built-in **Price Editor** so you can manage the whole
laptop list from an Excel sheet — no code.

## Open the editor

Go to your live site and add **`#admin`** to the end of the address, then press Enter:

```
https://YOUR-SITE-URL/#admin
```

(e.g. `https://vibejedi.github.io/pricelist/#admin`). A "🔧 JLS Price Editor"
window appears on top of the site. Close it anytime with **Close ✕** — visitors
never see it unless they type `#admin` themselves.

## The 4 steps

1. **⬇ Download Excel** — gives you `JLS-price-list.xlsx` with every laptop:
   brand, model, specs, **Price (PHP)**, **SRP (PHP)**, **Promo**, **Stock**.
2. **Edit in Excel or Google Sheets:**
   - **Price (PHP)** — selling price, numbers only (e.g. `89900`).
   - **SRP (PHP)** — original/strike-through price; leave blank for none.
   - **Stock** — `In stock`, `Pre-order`, or `Out of stock`.
   - **Promo** — small tag on the card (e.g. `2026 UPDATED PRICE`).
   - **Series** — the heading a laptop is grouped under on its brand page.
     Give two or more rows the **same Series** to bundle them under one heading
     (e.g. several `Vector 16 HX` configs). Leave it blank to let the laptop
     stand on its own (it groups by its Model name). This is independent of the
     Model text, so you can rename models freely without breaking the grouping.
   - Add a row for a new laptop, or delete a row to remove one.
   - **Keep the header row exactly as it is.**
3. **⬆ Import edited Excel** — loads your changes into a live preview and
   downloads an updated **`laptops.js`** file.
4. **Publish** — click **🐙 Open GitHub upload page**, drag `laptops.js` into the
   **`data`** folder, then **Commit changes**. The site updates in about a minute.

## Good to know

- The only file you ever re-upload is **`data/laptops.js`**. `index.html` (the
  design) never changes.
- **Photos are automatic:** just drop a model's images into its folder under
  `images/laptops/<folder>/` named `1.png`, `2.png`, … and upload them — the site
  shows whatever is there, no Excel or counts needed. See
  `images/laptops/FOLDERS.md` for each model's folder. (The **Photo Folder**
  column in the Excel is now only used if you want several models to share one
  set of photos, like the ROG Strix G16 configs.)
- **Brand-new model series:** a laptop only shows on the site if its brand +
  series already exists in the catalog inside `index.html`. Editing prices/specs
  of existing models always works; adding a never-before-seen *series* needs a
  one-line catalog edit — ask your developer.
- **Featured picks** (the 2 spotlighted laptops) are still set in `index.html`.
