# Maji Ndogo: Digital Twin Operations & Agricultural Analytics

## The Business Problem
The Ministry of Agriculture needed a reliable way to automate tractor navigation, manage variable fuel telemetry, and accurately track harvest records across disparate farms in the Maji Ndogo region. Manual logging and unhandled system telemetry errors frequently led to operational delays, unverified fuel shortages, and conflicting crop distribution records. 

To solve this, a Python-driven Digital Twin simulation was built to model field equipment operations, prevent system halts from missing telemetric inputs, and standardize crop inventory management across operations.

---

## The Tech Stack
* **Language:** Core Python (Python 3.13)
* **Design Approach:** Modular Function Design & Defensive Programming
* **Control Flow:** Conditional Logic, Dynamic Iteration (`for` / `while` loops)
* **Data Structures:** Python Dictionaries (Nested Lookups) and Sets (Set Operations & Uniqueness Constraints)
* **Environment:** VS Code & Jupyter Notebooks

---

## The Deliverable

### 1. Telemetry Handling & Defensive Logic
To ensure uninterrupted field navigation, system calculations must account for empty tanks and telemetry drops without raising runtime exceptions. The implementation uses explicit boundary checks to evaluate fuel levels safely before calculating consumption ratios.

| Defensive Logic Execution |
| :---: |
| ![Fuel Status Function](images/Screenshot%20(2).png) |
| *The `fuel_status()` function safely evaluates fuel capacity fractions, returning dynamic operational states ('Empty', 'Low', 'OK', 'Full') without risking runtime division errors.* |

### 2. Multi-Farm Inventory Reconciliation
Tracking seed varieties and crop plans across distinct agricultural zones previously created duplicate records and allocation conflicts. Using Python set theory operations (`intersection`, `difference`, `union`), crop distributions are automatically compared and reconciled.

| Set Operations for Crop Management |
| :---: |
| ![Compare Crop Plans](images/Screenshot%20(4).png) |
| *The `compare_crop_plans()` function uses set arithmetic to extract shared crops, identify unique regional varieties, and output clean, sorted yield categories.* |

### 3. Dynamic Yield & Harvest Tracking
Field data collection requires updating yields continuously as machinery returns from harvest runs. Using nested dictionary lookups, harvest entries automatically instantiate new farm records or increment existing crop yields cleanly.

| Nested Harvest Registry |
| :---: |
| ![Record Harvest Function](images/Screenshot%20(5).png) |
| *The `record_harvest()` pipeline updates nested dictionary keys dynamically, maintaining structured yield balances per farm ID without overwriting historical entries.* |

---

## The "So What?"
By replacing manual field logging with a structured Python digital twin, the system eliminates runtime crashes caused by unexpected telemetry anomalies. Automated set comparisons prevent duplicate seed purchases and conflicting field plans across regions, while dynamic dictionary indexing provides real-time visibility into harvest volumes across all participating farms in Maji Ndogo.
