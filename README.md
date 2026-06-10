# Highridge Construction Company — Weekly Payroll System

## Overview
This project was developed for **Highridge Construction Company** to automate the
generation of weekly payment slips for their workforce. It is implemented in both
**Python** and **R**.

---

## Files Included
| File | Description |
|------|-------------|
| `highridge_payroll.py` | Python payroll program |
| `highridge_payroll.R`  | R equivalent of the Python program |
| `README.md`            | This file |

---

## Features
- Dynamically generates a list of **400 workers** with randomised names, genders,
  and salaries.
- Iterates over every worker using a **for loop** to produce individual payment slips.
- Applies the following **employee-level classification rules**:
  - **A1** — Salary is greater than \$10,000 and less than \$20,000.
  - **A5-F** — Salary is greater than \$7,500 and less than \$30,000 **and** the
    employee is Female. *(This rule takes precedence over A1 when both conditions
    are satisfied.)*
- Includes **exception handling** to catch and report errors at both the worker and
  program level without crashing the entire run.

---

## How to Run

### Python
**Requirements:** Python 3.7 or later (no external libraries needed).

```bash
python highridge_payroll.py
```

Payment slips for all 400 workers will be printed to the terminal.

---

### R
**Requirements:** R 4.0 or later (base R only — no extra packages needed).

#### Option 1 — RStudio
1. Open `highridge_payroll.R` in RStudio.
2. Click **Source** (or press `Ctrl+Shift+Enter`).

#### Option 2 — Command Line
```bash
Rscript highridge_payroll.R
```

---

## Sample Output
```
=============================================
  HIGHRIDGE CONSTRUCTION COMPANY
  Weekly Payment Slip
=============================================
  Employee ID : 1
  Name        : Ngozi Worker1
  Gender      : Female
  Salary      : $18,432.75
  Level       : A5-F
=============================================
```

---

## Design Notes
- Workers are generated **dynamically** inside a helper function — no hard-coded list.
- The classification logic is isolated in its own function (`classify_employee`) to
  keep it readable and easy to modify.
- Exception handling wraps both the entire program and individual slip generation so
  a single bad record never aborts the whole run.

---

## Author
Software Engineer (Contracted)  
Highridge Construction Company Assignment — Module 1
