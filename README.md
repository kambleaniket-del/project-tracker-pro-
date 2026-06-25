# 🗂️ Project Tracker Pro — v1.0 (Intangles Analytics)

> **Enterprise-grade project management tool** — built as a single HTML file. No install, no server, no dependencies. Just open and use.

🔗 **Live App:** [https://kambleaniket-del.github.io/project-tracker-pro-/](https://kambleaniket-del.github.io/project-tracker-pro-/)

---

## ⚡ How to Run

### Option 1 — Online (Recommended)
Open the live link above in any modern browser. Works instantly — no login required.

### Option 2 — Local (Offline)
1. Download `index.html` from this repository
2. Double-click the file — it opens directly in your browser
3. All data saves automatically in your browser's local storage

> **Supported browsers:** Chrome 90+, Edge 90+, Firefox 88+, Safari 14+  
> **Best experience:** Chrome or Edge on a 1280px+ wide screen

---

## 📁 What's Pre-loaded

The app opens with **3 live Intangles Analytics projects** already loaded:

### 1. AID — Overboost
| Task | Owner | Status |
|------|-------|--------|
| Scoping the Algo | Waquar | Not Started |

### 2. Real Time Voltage Drop *(Active Project)*
| Task | Owner | Status | Progress |
|------|-------|--------|----------|
| Algo Changes | Akshay Bhivagade | ✅ Done | 100% |
| Combiner Changes | Ayush Mandhana | 🔵 In Progress | 95% |
| UX Changes | Anjali Pandey | ⬜ Not Started | 0% |
| Documentation *(child of UX)* | Anjali Pandey | ⬜ Not Started | 0% |
| New UI Changes | Anjali Pandey | ⚠️ At Risk | 0% |
| Final Release | — | 🔵 In Progress | 0% |

**Resources configured:** Ayush Mandhana · Anjali Pandey · Akshay Bhivagade  
**Dependencies:** New UI Changes → UX Changes (FS) · Final Release → New UI Changes (FS)

### 3. CARB
| Task | Owner | Status | Progress |
|------|-------|--------|----------|
| Revisit Documentation & build Test Cases | — | 🔵 In Progress | 65% |
| CSV & XML New format | — | 🔵 In Progress | 55% |
| Preparation for Application Document | — | ✅ Done | 100% |
| Submit Application | — | ⬜ Critical | 0% |

**Dependencies:** Submit Application → Preparation for Application Document (FS)

---

## 🖥️ Views

| View | How to Access | What it Shows |
|------|--------------|---------------|
| **Gantt** | Default view | Tasks, bars, dependencies, critical path |
| **Calendar** | Top nav → Calendar | Tasks laid out by month |
| **Team** | Top nav → Team | Resource-wise planner |
| **Network** | Top nav → Network | Dependency diagram (PERT-style) |
| **Roadmap** | Top nav → Roadmap | Cross-project timeline |
| **Dashboard** | Top nav → Dashboard | KPIs, burndown, status distribution |

---

## ✨ Key Features

### Gantt Chart
- **Drag bars** left/right to move tasks
- **Resize bars** from left or right edge to change duration
- **Drag rows** up/down using the `≡` handle to reorder tasks
- **Resize columns** — drag the column separator
- **Zoom** — D (day) / W (week) / M (month) buttons top-right
- **Critical path** — toggle with the CP button (turns red)
- **Baseline tracking** — save up to 5 named baselines, overlay on chart
- **Auto-schedule** — ⚡ Auto button cascades dependent task dates forward

### Task Management
- **Double-click any bar** or task row to open the edit modal
- Set status, priority, dates, progress, owner, notes, dependencies
- Add **milestones** (◆), **deadlines**, **recurrence**
- Assign **resources** with allocation %
- Add **custom fields** per task
- **Task comments** — threaded discussion per task

### Project Management
- **+ Project** button (sidebar) — add new projects
- **Export JSON** — full backup of all project data
- **Import JSON** — restore from backup
- **What-If Scenarios** — test date changes without affecting live data

### Reports
Access via the **Reports** button (toolbar):
- Slipping tasks · Overallocation · Milestones · Dependency health · Cross-project · Velocity

---

## 💾 Data & Storage

- All data saves **automatically** in your browser's `localStorage`
- Data is **per-browser** — opening on a different browser/computer starts fresh
- To **transfer data between computers**: use Export JSON → Import JSON
- **Each person who opens the live link gets their own private copy** of the data

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + Z` | Undo |
| `Ctrl + Y` | Redo |
| `Ctrl + S` | Save (auto-saves anyway) |
| `Double-click bar` | Open task editor |
| `Click + drag ≡` | Reorder task rows |

---

## 🎨 Themes & Appearance

Click the **theme button** (palette icon, toolbar) to choose from **28 themes**:

`Slate` · `Arctic` · `Nordic` · `Ivory` · `Sahara` · `Solar` · `Lemon` · `Matcha` · `Mint` · `Sakura` · `Lavender` · `Rose` · `Obsidian` · `Abyss` · `Carbon` · `Dracula` · `Midnight` · `Deep Sea` · `Forest` · `Ember` · `Copper` · `Rose Gold` · `Volcanic` · and more.

Also adjust **density** (Compact / Comfortable / Spacious) and **accent colour**.

---

## 🔒 Version Info

| Property | Value |
|----------|-------|
| Version | 1.0.0 LOCKED |
| Build date | 2026-06-25 |
| File | `index.html` (single file, ~375 KB) |
| Dependencies | None — zero external libraries |
| Browser storage | localStorage (auto-save) |

### Locked Fixes in this Version
| Fix | Description |
|-----|-------------|
| F01 | Gantt row alignment — DOM measurement syncs SVG bars to actual row heights |
| F02 | Status info moved onto Gantt bar (days · % · icon after bar) |
| F03 | Dependency arrow routing — FS overlap correctly routes below predecessor |
| F04 | Gantt horizontal scrollbar always visible |
| F05 | Timeline notes bar — theme-aware colours |
| F06 | Dark theme text contrast (Abyss, Carbon, Dracula, Copper, Volcanic) |
| F07 | Roadmap bar labels — readable in all themes |
| F08 | Cross-project dependency lines — fixed undefined function crash |
| F09 | Roadmap task names — full contrast in dark themes |
| F10 | Drag-to-reorder rows restored |

---

## 🛠️ For Developers

See the full developer guide inside `index.html` (search for `DEVELOPER GUIDE` in the source).

Key rules:
- Never use `i * ROW_H` to position SVG bars — use `_ry` / `_rh` from DOM measurement
- Never remove `position: relative` from `.task-row` — breaks drag handle
- Never add `overflow: hidden` to `.task-row` — clips drag handle
- Grid is 3 columns (WBS · Task · Owner) — do not add status column back
- Theme system: CSS vars AND JS `THEME_COLORS` object must both be updated for new themes

---

## 📞 Contact

**Aniket Kamble** — Analytics PM, Intangles  
📧 kamble.aniket@intangles.com  
🔗 [GitHub](https://github.com/kambleaniket-del/project-tracker-pro-)
