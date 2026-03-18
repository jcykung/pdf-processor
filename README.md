# PDF Processor

> Batch-stamp overlays onto student PDF reports — hide grades, add watermarks, insert logos, and more. **Build a template once, apply it to an entire class in seconds.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Visit%20Site-A6E22E?style=for-the-badge&logo=github)](https://jcykung.github.io/pdf-processor)
[![License](https://img.shields.io/badge/License-MIT-66D9EF?style=for-the-badge)](LICENSE)
[![No Dependencies](https://img.shields.io/badge/Dependencies-None-AE81FF?style=for-the-badge)](.)

---

## ✨ Features at a Glance

| Feature | Details |
|---|---|
| 🟥 Redact tool | Draw solid filled boxes to cover grades, scores, or any content |
| ✏️ Text tool | Add custom text labels with font, size, and colour control |
| 🖼️ Image tool | Stamp a PNG/JPG (e.g. school logo or seal) onto any page |
| 🕹️ Overlay scheduling | Control which pages each overlay appears on per student |
| 👁️ Ghost outlines | See faint previews of where overlays will land on other pages |
| 📐 Auto-scaling | Overlays scale automatically to match real page dimensions |
| ⭐ Favourites | Pin your most-used template so it's always pre-selected |
| ✏️ Inline rename | Rename templates directly from the template list |
| 🔍 Preview before download | Inspect every processed file before committing to a download |
| 💾 Backup & restore | Export all templates to a single `.json` file; restore with one click |

---

## 📖 How to Use

### 🖌️ Step 1 — Build a Template

Go to the **Template Editor** tab.

1. Click **Upload a Reference PDF** and open one student's report — it just needs the same layout as the rest of your class. The file is used as a visual guide only and is never modified.
2. Set **Pages/student** in the toolbar (use **−** / **+** or type directly). This tells the app how many pages belong to each student.
3. Draw overlays using the toolbar:

| Tool | Key | What it does |
|---|---|---|
| Redact | `R` | Draws a solid filled box — use it to hide grades or scores |
| Text | `T` | Places a text label; set font, size, and colour in the Properties panel |
| Image | `I` | Places a PNG or JPG — great for school logos or stamps |
| Pan | `P` | Scroll the canvas without accidentally placing anything |

> **Undo:** `Ctrl Z` &nbsp;|&nbsp; **Redo:** `Ctrl Y` &nbsp;|&nbsp; On Mac, use `⌘` in place of `Ctrl`

4. Click any overlay to open the **Properties** panel and set **When to show this**:

| Setting | Behaviour |
|---|---|
| Once per student | Appears on the same page position for every student *(use this for most overlays)* |
| This page and all after | Repeats from this page to the last page of each student's block |
| Every single page | Appears on every page in the entire PDF — good for watermarks |
| Specific pages only | You type which pages (e.g. `1, 3-5`) per student |

5. Type a name in the toolbar field (e.g. `Grade 9 Reports 2025`) and click **Save**. You'll see a **● Saved** flash to confirm. There is no autosave — always click Save after making changes.

---

### ⚙️ Step 2 — Process Your Reports

Go to the **PDF Processor** tab.

1. **Choose Template** — click your template in the list to select it (highlights orange). Your starred favourite will be pre-selected automatically.
2. **Pages Per Student** — confirm the number matches what you used in the Template Editor. If this is wrong, overlays will appear on the wrong pages.
3. **Process Reports** — drag-and-drop or select all your student PDFs at once. Click **▶ Process & Preview**.
4. A preview renders each processed file. Check it looks right, then click **⬇ Download All** (or **⬇ Download This One** for individual files).

> You can also process students submitted as **separate PDF files** — just add them all in Step 3 and set Pages Per Student to however many pages each file contains.

---

## 🗂️ Managing Your Templates

All saved templates appear in the **1. Choose Template** card on the PDF Processor tab.

| Action | How |
|---|---|
| ⭐ Favourite | Click the star to pin a template to the top; it will be pre-selected on next open |
| ✏️ Rename | Hover a template row and click the pencil icon to rename it in place |
| 🗑 Delete | Hover a template row and click the bin icon to permanently remove it |
| ✏️ Edit overlays | Hover a template row and click **Edit** — opens the Template Editor with that template loaded |

> Changes in the Template Editor are **not saved until you click Save**.

---

## ❓ Common Questions

**My overlays are appearing on the wrong pages.**  
The most common cause is a mismatched **Pages Per Student** value. Make sure the number in the Template Editor toolbar and Step 2 on the Processor tab are identical.

**My templates disappeared after I cleared my browser history.**  
Templates are stored in `localStorage`, which is wiped when you clear browsing data. Use **⬇ Backup All** regularly and keep the `.json` file somewhere safe (e.g. Google Drive). Restore everything at once with **Load Backup File** on the PDF Processor tab.

**Does this work for any PDF, or only JumpRope reports?**  
It works with any PDF. As long as each student's section has the same number of pages and roughly the same layout, it will work perfectly. It was originally designed for [JumpRope](https://jumpro.pe/) reports.

**My students' reports have different page counts. Will this work?**  
The tool requires a consistent page count per student in a single run. The easiest fix is to export reports with a **Duplex** or **Fixed pages** option in your report software so every student gets the same count. In JumpRope, choose **Duplex** when generating reports.

---

## ⚠️ Important: Browser Storage is Temporary

Templates are stored in your browser only. Clearing browser history, switching browsers, or using a new device will wipe everything.

**✅ To keep your templates permanently:**

Click **⬇ Backup All** (bottom of the left sidebar) to download a single `.json` file containing all your templates. Save it to your computer or Google Drive. To restore, use **Load Backup File** on the PDF Processor tab — all templates will be imported at once.

---

## 🏗️ Tech Stack

| | |
|---|---|
| **Framework** | None — plain HTML, CSS, and vanilla JavaScript |
| **PDF rendering** | [PDF.js](https://mozilla.github.io/pdf.js/) |
| **PDF export** | [pdf-lib](https://pdf-lib.js.org/) |
| **Storage** | Browser `localStorage` |

---

## 🌐 Browser Support

| Browser | Supported |
|---|---|
| Chrome / Edge | ✅ Fully supported |
| Firefox | ✅ Fully supported |
| Safari (macOS) | ✅ Fully supported |
| Safari (iOS) | ⚠️ May have PDF download limitations |
| Android Chrome | ⚠️ May have PDF download limitations |

> Best experienced on **desktop Chrome or Edge**.

---

## ☕ Support

I'm a full-time teacher who builds tools like this in my spare time. If PDF Processor saves you even a few minutes, I'd really appreciate a coffee!

[![Ko-fi](https://img.shields.io/badge/Ko--fi-Support%20this%20project-F92672?style=for-the-badge&logo=ko-fi)](https://ko-fi.com/coolpuddytat)

---

## 📄 License

MIT — free to use, modify, and distribute. Attribution appreciated but not required.

---

*Built with ❤️ by [Jonathan Kung](https://ko-fi.com/coolpuddytat)*
