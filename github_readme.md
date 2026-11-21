# SQL Interview Studio

An interactive, zero-setup SQL coding interview prep platform built for aspiring **Business Analysts**, **Data Analysts**, and **Data Engineers**. Practice **30 curated real-world SQL challenges** across **Easy**, **Medium**, and **Hard** difficulty tiers directly in your browser—complete with live database tables, an in-browser SQLite engine, and an automated diagnostic query debugger.

🔗 **Live App:** `https://<your-github-username>.github.io/sql-interview-studio/`

---

## ✨ Key Features

- **30 Curated SQL Interview Challenges:**
  - **Easy (1–10):** `WHERE` vs. `HAVING`, `CASE WHEN` categorization, duplicate detection, inclusive date range filtering, unit-price vs. aggregate filtering, `COALESCE` single & multi-column fallbacks, and foundational `LEFT JOIN + IS NULL` anti-joins.
  - **Medium (11–20):** Regional & catalog anti-joins, the **Anti-Join "Bouncer" Pattern** (`LEFT JOIN ... ON ... AND`), zero-preserving `COALESCE(SUM(...), 0)` reports, conditional `SUM(CASE WHEN ...)`, zero-safe percentages (`100.0 / NULLIF(..., 0)`), and CTE cohort conversion rates.
  - **Hard (21–30):** Window functions (`ROW_NUMBER()`, `DENSE_RANK()`, `LAG()`), Top-N leaderboards with ties, consecutive period-over-period comparisons, and multi-CTE data transformation pipelines.
- **Real In-Browser SQL Execution (`sql.js`):** Runs actual SQLite queries client-side via WebAssembly. Every problem initializes a clean, isolated database pre-loaded with realistic sample rows and edge cases (`NULL`s, zero-activity entities, ties, and multi-period dates).
- **Smart Diagnostic Checker ("Why You Are Incorrect"):** Instead of just saying *Wrong Answer*, the verifier compares your output and SQL structure against the reference solution to pinpoint common interview mistakes:
  - Missing, misspelled, or extra helper columns (e.g., leaving `rn` in the outer `SELECT`)
  - Anti-join filter placement traps (`WHERE` vs. `LEFT JOIN ... ON`)
  - `NULL` vs. `0` aggregation discrepancies (`COALESCE`)
  - Integer division truncation (`100.0 / NULLIF(..., 0)`)
  - Row sorting (`ORDER BY`) mismatches with a side-by-side result diff table
- **Built-In SQL Interview Cheat Sheet:** Quick-reference modal covering SQL clause execution order, anti-join rules, zero-safe math, CTE scope, and window function anatomy.
- **100% Private, Local Progress:** All query drafts and solved badges are stored locally in your browser's `localStorage`—every visitor gets their own personal sandbox without affecting anyone else.

---

## 🛠️ Tech Stack

- **Frontend:** HTML5, Tailwind CSS (CDN), Vanilla JavaScript (ES6+)
- **Database Engine:** [sql.js](https://github.com/sql-js/sql.js/) (SQLite compiled to WebAssembly)
- **Typography:** Inter & JetBrains Mono
- **Hosting:** Zero-build single-file architecture (`index.html`) designed for GitHub Pages

---

## 🚀 Run Locally or Deploy to GitHub Pages

Because **SQL Interview Studio** is packaged into a single standalone `index.html` file with no build step or backend server required, you can run or host it anywhere in seconds:

### Run Locally
1. Clone or download this repository:
   ```bash
   git clone https://github.com/<your-github-username>/sql-interview-studio.git
   ```
2. Open `index.html` directly in any modern web browser (Chrome, Edge, Firefox, Safari).

### Host Your Own Copy on GitHub Pages
1. Fork or upload `index.html` to a public GitHub repository named `sql-interview-studio`.
2. Navigate to **Settings → Pages**.
3. Under **Build and deployment → Source**, select **Deploy from a branch**, pick **`main`** and **`/ (root)`**, and click **Save**.
4. Your live platform will be available at `https://<your-github-username>.github.io/sql-interview-studio/`.

---

## 📚 Curriculum Overview

| Tier | Problems | Core SQL Concepts Covered |
| :--- | :---: | :--- |
| **Easy** | #1 – #10 | `SELECT`, `WHERE`, `GROUP BY`, `HAVING`, `CASE WHEN`, `COALESCE`, `LEFT JOIN + IS NULL` |
| **Medium** | #11 – #20 | Anti-Join `ON` Filters, `COUNT(DISTINCT CASE WHEN ...)`, `NULLIF`, `ROUND`, Single-CTE Aggregations |
| **Hard** | #21 – #30 | `ROW_NUMBER()`, `DENSE_RANK()`, `LAG()`, Time-Series Deltas, Chained Multi-CTE Pipelines |

---

## 🤝 Contributing

Have an idea for a new SQL interview pattern or edge case? Feel free to open an issue or submit a pull request!

## 📄 License

This project is open source and available under the [MIT License](LICENSE).