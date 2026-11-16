# Excel Practice Lab — Learn Excel by Doing

> **Independent Educational Portfolio Project**  
> *Not affiliated with, endorsed by, or owned by Microsoft Corporation.*

Excel Practice Lab is an advanced, client-side, browser-based spreadsheet application and Excel training platform designed for students, beginners, job seekers, and aspiring Data Analysts. It provides a real spreadsheet engine with over 60 Excel functions, dynamic arrays, interactive pivot tables, charts, data cleaning tools, 32 automated practice exercises, and 11 business datasets—all functioning without Microsoft Excel or backend servers.

---

## 🔒 Zero Data Storage Architecture (Privacy by Design)

Excel Practice Lab operates as a strictly stateless, client-side application:

1. **No backend databases:** Zero servers, Firebase, Supabase, or cloud persistence.
2. **No browser databases:** Zero IndexedDB, LocalStorage, or SessionStorage for user workbooks.
3. **No tracking cookies:** Zero user tracking, accounts, or telemetry.
4. **100% In-Memory Processing:** All calculations, cell modifications, and undo/redo stacks run in JavaScript memory during your active browser tab session.
5. **Direct Client-Side I/O:** Import `.xlsx`, `.xls`, and `.csv` files locally via browser file reading APIs. Export directly to your computer's downloads folder.
6. **Unsaved Warning Guard:** If you try to refresh or leave the tab with unsaved modifications, the browser alerts you to download your workbook first.

> **Privacy Notice Displayed in Application:**  
> *"Your data stays in your browser. Excel Practice Lab does not save or upload your spreadsheets. Download your workbook before leaving the page."*

---

## 🚀 Key Features

### 1. Spreadsheet Grid & Workspace
- **Virtualized Grid:** High-performance rendering of rows and columns with fixed, sticky headers.
- **Cell Selection & Editing:** Single cell selection, multi-cell range drag selection, fill handle autofill, double-click inline editing, and formula bar editing.
- **Row & Column Operations:** Drag handles for row height and column width resizing, insert/delete row/column, hide/unhide, freeze panes.
- **Multiple Worksheets:** Create, rename, duplicate, delete, reorder, and color-code multiple sheets per workbook.
- **Keyboard Shortcuts:** Full spreadsheet keyboard navigation (`Arrow Keys`, `Tab`, `Enter`, `F2`, `Delete`, `Ctrl+C`, `Ctrl+V`, `Ctrl+Z`, `Ctrl+Y`, `Ctrl+F`, `Ctrl+A`).
- **Formatting Toolbar:** Font family, font size, bold, italic, underline, custom text/fill color pickers, cell borders, text alignments, text wrapping, and number formatting (General, Currency `$`, Percentage `%`, Date `YYYY-MM-DD`, Decimals).

### 2. Comprehensive Formula Engine
Built with a recursive-descent expression parser and circular reference cycle detection (`#CIRCULAR!`), supporting:
- **Mathematical:** `SUM`, `PRODUCT`, `ABS`, `ROUND`, `ROUNDUP`, `ROUNDDOWN`, `INT`, `MOD`, `POWER`, `SQRT`, `SUBTOTAL`.
- **Statistical:** `AVERAGE`, `MEDIAN`, `MODE`, `MIN`, `MAX`, `COUNT`, `COUNTA`, `COUNTBLANK`, `STDEV`, `STDEV.S`, `STDEV.P`, `VAR`, `VAR.S`, `VAR.P`.
- **Logical:** `IF`, `IFS`, `AND`, `OR`, `NOT`, `IFERROR`, `IFNA`, `TRUE`, `FALSE`.
- **Conditional:** `SUMIF`, `SUMIFS`, `COUNTIF`, `COUNTIFS`, `AVERAGEIF`, `AVERAGEIFS`.
- **Lookup & Reference:** `VLOOKUP`, `HLOOKUP`, `XLOOKUP`, `INDEX`, `MATCH`, `CHOOSE`, `ROW`, `COLUMN`, `ROWS`, `COLUMNS`.
- **Text:** `LEFT`, `RIGHT`, `MID`, `LEN`, `TRIM`, `CLEAN`, `UPPER`, `LOWER`, `PROPER`, `CONCAT`, `CONCATENATE`, `TEXTJOIN`, `FIND`, `SEARCH`, `SUBSTITUTE`, `REPLACE`, `TEXT`, `VALUE`.
- **Date & Time:** `TODAY`, `NOW`, `DATE`, `DAY`, `MONTH`, `YEAR`, `DATEDIF`, `EOMONTH`, `EDATE`, `WEEKDAY`, `WEEKNUM`, `WORKDAY`, `NETWORKDAYS`.
- **Dynamic Arrays:** `FILTER`, `SORT`, `SORTBY`, `UNIQUE`, `SEQUENCE`, `TRANSPOSE`.
- **Real-Time Formula Autocomplete:** Suggests formula names and argument syntax as you type `=`.

### 3. Data Cleaning & Management
- **Remove Duplicate Rows:** Identifies duplicate records across selected columns.
- **Remove Blank Rows:** Cleans empty lines with 1 click.
- **Trim Whitespace:** Strips leading, trailing, and duplicate spaces.
- **Case Converter:** Transform text to `UPPER`, `lower`, or `Proper` casing.
- **Text to Columns Wizard:** Split delimited strings (comma, space, tab, semicolon, custom) across adjacent columns with real-time preview.
- **Find and Replace:** Search by text or number with case matching and whole-cell matching.
- **Data Validation:** Dropdown lists from comma-separated items, numeric range constraints, text length rules, and error warnings.
- **Conditional Formatting:** Greater than, less than, equal to, text contains, duplicate values, unique values, data bars, and gradient color scales.

### 4. Advanced Analytics & Visualization
- **Interactive Pivot Tables:** Source range selector, row fields, column fields, and values with `SUM`, `COUNT`, `AVERAGE`, `MIN`, `MAX` aggregations, generating cross-tabs with row and column totals and 1-click "Insert as New Sheet".
- **Dynamic Chart Builder:** Responsive charts powered by Recharts (Column, Bar, Line, Area, Pie, Scatter) with custom titles, series selection, and legends.
- **Statistical Analytics Workbench:** Descriptive statistics (Count, Sum, Mean, Median, Mode, Variance, Standard Deviation, Min, Max, Range), frequency distribution histograms, Pearson correlation coefficient, and simple linear regression ($y = mx + c$).

### 5. Excel Academy (Learn by Doing)
Structured across 5 progressive levels with theory, syntax guides, real-world examples, and 1-click "Open in Practice Sandbox" buttons:
- **Level 1:** Excel Fundamentals
- **Level 2:** Basic Formulas
- **Level 3:** Intermediate Excel
- **Level 4:** Advanced Excel (Lookups & Logic)
- **Level 5:** Professional Analytics & BI

### 6. Practice Lab (32 Interactive Exercises)
32 original challenges across Beginner, Intermediate, and Advanced tiers. Each exercise contains a scenario, working dataset, automated test validator that inspects evaluated cell results, hints, detailed explanations, and instant celebration feedback.

### 7. 11 Realistic Business Datasets
Pre-bundled datasets ready to load or download as CSV:
1. Employee Records (HR compensation & performance)
2. Sales Transactions (Regional reps, units, revenue)
3. Customer Information (Segments, lifetime spend)
4. Product Inventory (SKUs, stock, reorder formulas)
5. Student Marks & Grades (Test scores, grade formulas)
6. Attendance Records (Hours logged, overtime)
7. Monthly Department Expenses (Budget vs Actual variance)
8. E-commerce Orders (Payment methods, discounts)
9. HR Payroll Summary (Taxes, bonuses, net pay)
10. Marketing Campaign Data (CTR, impressions, conversions)
11. Messy Dataset (Erratic spaces, blanks, duplicates for cleaning)

---

## 🛠️ Technology Stack

- **Framework:** React 19 + TypeScript
- **Bundler:** Vite 8 (Rolldown engine)
- **Styling:** Tailwind CSS v4
- **Icons:** Lucide React
- **File I/O:** SheetJS (`xlsx` Apache 2.0) & PapaParse (MIT)
- **Data Visualization:** Recharts (MIT)
- **Testing:** Vitest (19 automated unit tests)
- **Hosting / Deployment:** Netlify Free Tier (`netlify.toml` + `_redirects`)

---

## 💻 Local Development Instructions

### Prerequisites
- Node.js `v18+` or `v20+` (tested on Node v24)
- npm `v9+` or `v11+`

### Installation
```bash
# Clone the repository
git clone <repo-url>
cd kunal

# Install dependencies
npm install
```

### Running Locally
```bash
# Start development server
npm run dev
```
Open `http://localhost:5173` in your browser.

### Running Automated Tests
```bash
npm test
```

### Production Build
```bash
npm run build
```
Generates optimized static assets in the `dist/` directory.

---

## 🌐 Netlify Deployment Instructions

The repository is pre-configured with `netlify.toml` and `public/_redirects` for continuous deployment on Netlify's free hosting tier:

1. **Push your code to GitHub / GitLab / Bitbucket.**
2. Log in to [Netlify](https://app.netlify.com/).
3. Click **"Add new site"** → **"Import an existing project"**.
4. Select your Git repository.
5. Verify the deployment settings:
   - **Build command:** `npm run build`
   - **Publish directory:** `dist`
6. Click **"Deploy site"**. Netlify will build and deploy the SPA in under 1 minute with automatic HTTPS and global CDN delivery.

---

## ⚠️ Known Limitations & Future Improvements

### Known Limitations
- Macro execution (VBA / Office Scripts) is not supported in browser-only web environments for security and sandboxing reasons.
- Highly specialized Analysis Toolpak statistical distributions (e.g., two-way ANOVA, Fourier transforms) are simplified to descriptive statistics and linear regression.
- Workbooks exist in-memory; closing the tab without exporting to `.xlsx` or `.csv` discards in-memory modifications by intentional design.

### Future Improvements
- Multi-user peer-to-peer WebRTC live collaboration without server storage.
- Additional financial functions (`XIRR`, `XNPV`, `PMT`, `NPER`).
- Custom formula syntax highlighting inside the grid cells while editing.
