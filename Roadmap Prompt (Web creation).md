**Role:** Expert Frontend Developer specializing in React and Creative UI Design.

**Task:** Create a "Single File" HTML application for a "Student Data Analyst Roadmap". The application must use React (via CDN), Tailwind CSS (via CDN), and Lucide Icons.

**Technical Constraints:**
1.  **Single File:** All HTML, CSS, and JavaScript must be contained in one `index.html` file. No external builds (npm/webpack). Use Babel standalone.
2.  **Persistence:** Use `localStorage` to save the user's progress (checkbox states) so data isn't lost on refresh. 
    * *Critical:* Wrap the `JSON.parse` logic in a `try-catch` block to prevent the app from crashing if data is corrupted.

**Design Aesthetic (Theme):**
* **Colors:** Dark mode base using "Stone-900" (`#1c1917`) and "Stone-800" (`#292524`). Accents should be gradients of Amber/Gold (`#fbbf24`) to Orange (`#ea580c`).
* **Vibe:** Premium, immersive, "Interstellar/Space" feel.
* **Background:** CSS-generated star field or subtle texture.
* **Effects:**
    * **Glassmorphism:** Use translucent backgrounds with blur for cards.
    * **3D Tilt:** Implement a mouse-move parallax effect on the main cards so they tilt in 3D space when hovered.
    * **3D Cube:** A purely CSS-animated rotating 3D cube in the hero section displaying icons on its faces.

**Core Features & Functionality:**
1.  **Progress Tracking:**
    * A circular progress bar in the hero section showing the total % completed.
    * A linear progress bar on *each card* showing the % completed for that specific month.
    * Visual feedback: When a month is 100% complete, the card border should turn Green/Emerald and glow.
2.  **Accordion Interaction (CRITICAL FIX):**
    * The months should be displayed as cards.
    * **Click Logic:** The click event to expand/collapse the card must be attached **ONLY to the Header section** of the card (the title/icon area). 
    * **Do NOT** attach the click listener to the entire card container. This is to ensure that clicking checklists or links inside the body does not accidentally collapse the card.

**Content Data Structure (Must Use Exactly This):**

Create a `ROADMAP_DATA` constant with this exact data structure. Render resources as `<a>` tags with `target="_blank"`.

**Phase 1: Foundations** (Subtitle: Excel & Statistics)
* *Description:* The starting point. Master data organization and basic analysis math.
* *Topics/Checklist:*
    * Excel: VLOOKUP & Pivot Tables
    * Excel: Data Cleaning & Power Query
    * Stats: Mean, Median, Mode & Std Dev
    * Stats: Distributions & p-values
* *Resources:*
    * WSCube Tech (Excel) [Urdu/Hindi] -> `https://www.youtube.com/@wscubetechjodhpur`
    * Codanics (Stats) [Urdu/Hindi] -> `https://www.youtube.com/@Codanics`
    * Excel Easy [English] -> `https://www.excel-easy.com/`

**Phase 2: SQL Mastery** (Subtitle: Database Querying)
* *Description:* Learn how to talk to databases and pull specific information.
* *Topics/Checklist:*
    * SQL: SELECT, FROM, WHERE
    * SQL: Joins (Inner, Left, Right)
    * SQL: GROUP BY & Aggregations
    * SQL: CTEs & Subqueries
* *Resources:*
    * CodeWithHarry (SQL) [Hindi] -> `https://www.youtube.com/@CodeWithHarry`
    * Technical Suneja [Hindi] -> `https://www.youtube.com/@TechnicalSuneja`
    * SQLZoo Practice [English] -> `https://sqlzoo.net/`

**Phase 3: Visual Storytelling** (Subtitle: BI Tools (Power BI/Tableau))
* *Description:* Turn your data into beautiful, interactive charts and maps.
* *Topics/Checklist:*
    * Connecting Data Sources
    * Creating Interactive Dashboards
    * DAX / Calculated Fields
    * Color Theory & UI Design
* *Resources:*
    * Skillsiya (Power BI) [Hindi] -> `https://www.youtube.com/@Skillsiya`
    * Codanics (Tableau) [Urdu] -> `https://www.youtube.com/@Codanics`
    * Storytelling with Data [English] -> `https://www.storytellingwithdata.com/`

**Phase 4: Python for Data** (Subtitle: Programming & Pandas)
* *Description:* Use code to automate cleaning and analysis for huge datasets.
* *Topics/Checklist:*
    * Python: Loops & Functions
    * Pandas: DataFrames
    * Data Cleaning with NumPy
    * Matplotlib & Seaborn
* *Resources:*
    * Codebasics (Python) [Hindi] -> `https://www.youtube.com/@codebasics`
    * CodeWithHarry (Python) [Hindi] -> `https://www.youtube.com/@CodeWithHarry`
    * Kaggle Python Course [English] -> `https://www.kaggle.com/learn/python`

**Phase 5: Portfolio Building** (Subtitle: Real World Projects)
* *Description:* Build your own project to show future employers what you can do.
* *Topics/Checklist:*
    * Find a Dataset on Kaggle
    * End-to-End Data Cleaning
    * Build Final Dashboard
    * Upload Code to GitHub
* *Resources:*
    * Codebasics Projects [Hindi] -> `https://www.youtube.com/@codebasics`
    * Kaggle Datasets [English] -> `https://www.kaggle.com/datasets`

**Phase 6: Interview Prep** (Subtitle: Resume & Job Search)
* *Description:* Final polish for your resume and practicing interview questions.
* *Topics/Checklist:*
    * Advanced SQL (Window Functions)
    * KPIs & Business Metrics
    * Optimizing LinkedIn Profile
    * Behavioral Mock Interviews
* *Resources:*
    * WSCube Tech (Careers) [Hindi] -> `https://www.youtube.com/@wscubetechjodhpur`
    * Data Analyst Resume Guide [English] -> `https://www.freecodecamp.org/news/tag/resume/`

**Code Structure:**
* Create a `<TiltCard>` component for the 3D effect.
* Create the main `<App>` component.
* Ensure the checkboxes use a custom animation (scale pop) when clicked.