# Farabi HR Management System – Frontend UI Redesign

Enterprise-grade HR & Clinic Management System UI featuring a modern design language (Linear/Stripe aesthetic), pixel-perfect layout shells, self-hosted web fonts, and full English / Arabic (RTL) support.

---

## 🚀 Quick Start (Running Locally)

This project has **zero external build dependencies or npm build steps** — it runs out of the box with any HTTP static server.

### 1. Clone the repository
```bash
git clone https://github.com/blackbaster-dot/Farabi-HR-New-Design_-Vibe-coded.git
cd Farabi-HR-New-Design_-Vibe-coded
```

### 2. Start a local server

**Using Python (built into Mac/Linux):**
```bash
python3 -m http.server 3000
```

**Using Node.js / npx:**
```bash
npx serve -l 3000
```

### 3. Open in Browser
- **Shifts & Presets:** [http://localhost:3000/shifts.html](http://localhost:3000/shifts.html)
- **Users Directory:** [http://localhost:3000/users.html](http://localhost:3000/users.html)
- **My Requests:** [http://localhost:3000/index.html](http://localhost:3000/index.html)
- **Executive Dashboard:** [http://localhost:3000/dashboard.html](http://localhost:3000/dashboard.html)

---

## 📂 Project Structure & Key Files

```text
├── index.html          # "My Requests" Screen: Filter pills, data table, tooltips, collapsible cards
├── shifts.html         # "Shifts & Presets" Screen: Farabi branding, dual English/Arabic hours, clock rules
├── users.html          # "Users Directory" Screen: Bilingual roles, search/filters, contact details
├── dashboard.html      # "HR Dashboard" Screen: Attendance analytics, capacity bars, urgent approvals
├── fonts/              # Self-hosted WOFF2 fonts for offline & fast rendering
│   ├── bricolage-grotesque.woff2       # Primary English font (Variable weights 400-700)
│   ├── ibm-plex-sans-arabic-400.woff2  # Arabic Regular
│   ├── ibm-plex-sans-arabic-600.woff2  # Arabic SemiBold
│   └── ibm-plex-sans-arabic-700.woff2  # Arabic Bold
└── README.md           # Developer handover documentation
```

---

## 🎨 Design System & Architecture Specifications

### 1. App-Shell & Scroll Model
- **No Window Scroll:** `html, body` are set to `height: 100dvh; overflow: hidden;`.
- **Sidebar:** Left column (`230px` width, collapsible to `68px`), warm off-white (`#F5F4F0`).
- **Main Panel:** Pure white (`#FFFFFF`) with a `16px` rounded top-left corner (`border-top-left-radius: 16px;`).
- **Pinned Header:** Pin-positioned header (`height: 60px;`) with breadcrumb and user profile that never scrolls.
- **Scroll Container:** Independent scrolling container (`flex: 1; overflow-y: auto;`) with `56px` padding margin (`--page-margin: 56px;`).
- **Sticky Table Headers:** `position: sticky; top: 0; z-index: 5;` with solid background so scrolling rows never show through.

### 2. Typography Tokens
- **English Font:** `Bricolage Grotesque, sans-serif` (Self-hosted in `fonts/`).
- **Arabic Font:** `IBM Plex Sans Arabic, Noto Sans Arabic, sans-serif` (Self-hosted in `fonts/`).
- **RTL Support:** Toggling `dir="rtl"` dynamically mirrors the sidebar, breadcrumbs, search inputs, tables, and typography via the `文A` toggle button.

### 3. Key Components
- **Collapsible Metric Cards:** Smooth cubic-bezier transition (`max-height`, `opacity`, and `margin`) with state persistence in `localStorage`.
- **Data Tables:** Custom checkboxes, status indicators, copy-to-clipboard IDs, two-line approver/shift cells, and action triggers.
- **Floating Settings Trigger:** Farabi brand settings button anchored to the right edge.

---

## 🔗 Design References & Figma File
- **Figma Source:** [Farabi HR System – Redesign](https://www.figma.com/design/iIPbNtYsBvTboLoa10yGhm/Farabi-HR-System-%E2%80%93-Redesign?node-id=25-10)
- **Editable Figma Artboards:** Located on the `Web Playground` page under the section `Farabi HR – Shifts & Presets (Editable Artboard)` and `Farabi HR – Users Directory (Editable Artboard)`.
