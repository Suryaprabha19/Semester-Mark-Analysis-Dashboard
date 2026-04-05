# 🎓 CSE Sem1 Marks Dashboard Analysis
An Excel-based academic marks analysis and dashboard for **63 CSE Semester 1 students**, featuring subject-wise Pass/Fail pie charts, overall performance tracking, CGPA calculation, and an interactive student filter.

---

## 📁 File

```
Sem1_Marks.xlsx
```

---

## 🗂️ Workbook Structure

The workbook contains **15 sheets** organized as follows:

| Sheet | Purpose |
|-------|---------|
| `Marks` | Master data — student register numbers, names, grades, CGPA, pass/fail formulas |
| `Dashboard` | Visual dashboard with pie charts and student slicer |
| `Sheet2–Sheet14` | Pivot tables powering each subject's Pass/Fail chart |

---


## 📊 Dashboard Overview

The dashboard provides:

- **Total Students** — 63
- **Overall Pass vs Fail** pie chart — 56 Pass (89%), 7 Fail (11%)
- **Subject-wise Pass/Fail** pie charts for all 9 subjects
- **Interactive Student Name Slicer** — filter all charts by individual student

### Subject-wise Pass/Fail Summary

| Subject | Pass | Fail | Pass % |
|---------|------|------|--------|
| GE3172 (Lab) | 63 | 0 | 100% |
| HS3152 | 63 | 0 | 100% |
| BS3171 | 63 | 0 | 100% |
| MA3151 | 61 | 2 | 97% |
| GE3151 | 61 | 2 | 97% |
| GE3152 | 60 | 3 | 95% |
| CY3151 | 62 | 1 | 98% |
| PH3151 | 59 | 4 | 94% |
| **Overall** | **56** | **7** | **89%** |

---

## 🧮 How the Marks Sheet Works

### Grade to Points Conversion
Each subject grade is converted to grade points using nested `IF` formulas:

```
O  → 10
A+ → 9
A  → 8
B+ → 7
B  → 6
C  → 5
U  → 0  (Fail)
```

### Pass/Fail Logic
- **Theory subjects** — Pass if grade is O, A+, A, B+, B, or C; Fail only if U
- **Lab subjects** — Pass if grade is not U
- **Overall** — Fail if any single subject grade point equals 0

### CGPA
Each student's CGPA is pre-calculated and stored in the `CGPA` column.

---

## 🔍 Key Columns in the `Marks` Sheet

| Column | Description |
|--------|-------------|
| Register Number | Student's unique ID (e.g., 953623104002) |
| Name of the Student | Full name |
| HS3152 – GE3172 | Letter grades for each subject |
| CGPA | Cumulative Grade Point Average |
| English – Eng Lab | Numeric grade points (formula-computed) |
| Eng – EL | Pass/Fail status per subject (formula-computed) |
| Overall | Overall Pass/Fail result |

---

## ✨ Features

- 📌 **Interactive slicer** to filter all charts by student name
- 🥧 **9 subject-wise pie charts** showing Pass/Fail distribution
- 📐 **Formula-driven** — grade points and pass/fail auto-update when grades change
- 🏫 Designed for **CSE Department** academic reporting

---

## 🛠️ Tools Used

- **Microsoft Excel** — Pivot Tables, Pie Charts, Slicers, IF Formulas

---

## 📝 Notes

- A student is marked **Fail overall** only if they have a `U` in **any single subject**.
- Lab subjects (GE3171, BS3171, GE3172) achieved a **100% pass rate**.
- **PH3151 (Physics)** had the most failures — 4 students (6%).
- Data belongs to the **CSE Department, Batch 2023**, Semester 1.

---

## 📄 License

This file is intended for internal academic use by the Department of CSE.
