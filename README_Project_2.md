# 🎓 Enterprise LMS Early Warning & Academic Analytics Pipeline

An automated data engineering and analytics pipeline designed for Higher Education institutions to monitor student LMS activity, detect early-stage drop-out risks, and dispatch actionable intervention lists to academic counseling departments.

## 📌 Executive Problem Solved
Traditional gradebooks only capture academic failure after exams are complete. This pipeline combines **academic performance** (grades) with **behavioral engagement** (LMS clickstream timestamps) to flag disengaged and at-risk students weeks before course failure occurs.

## 🛠️ Architecture & Tech Stack
- **Database Layer:** SQLite relational database (Students, Courses, Enrollments, Clickstream Server Logs).
- **Data Engineering:** Python, Pandas (3-way relational SQL Joins, data sanitization, date math).
- **Analytics & Risk Engine:** Multi-factor logic matrix classifying students into 4 distinct risk tiers.
- **Visualization:** Matplotlib, Seaborn (4-panel Executive Dashboard & Engagement Matrix).
- **Automated Dispatch:** Scheduled CSV report generator with dynamic timestamping.

## 📊 4-Tier Risk Classification Matrix
1. **🔴 CRITICAL:** Grade $< 50\%$ AND Inactive $\ge 5$ Days (Immediate Intervention Required).
2. **🟠 ACADEMIC RISK:** Grade $< 50\%$ but actively logging in (Tutoring Support Required).
3. **🟡 ENGAGEMENT RISK:** Passing grade but Inactive $\ge 5$ Days (Retention Check-in Required).
4. **🟢 GOOD STANDING:** Passing grade and active on portal within 48 hours.

---
*Created as Project 2 in my 60-Day Educational Technology Systems & Analytics Mastery Portfolio.*
