# Maji Ndogo: Python Foundations & Digital Twin Simulation

## Project Overview
Designed and implemented core Python logic for an agricultural digital twin system simulating tractor operations, fuel status tracking, and field navigation for the Maji Ndogo water analytics project.

---

## Key Technical Implementations
* **Defensive Fuel Logic:** Designed dynamic functions (e.g., `fuel_status()`) incorporating safety checks to eliminate zero-division errors and manage missing telemetry data.
* **Automated Field Navigation:** Built iteration pipelines using `for` and `while` loops to map tractor coordinates across agricultural fields and navigate obstacles.
* **Structured Data Management:** Employed Python dictionaries and sets to aggregate crop data, look up field metadata, and maintain lists of unique assets efficiently.

---

## Reflection & Technical Interview Q&A

### Q1: Why check if the fuel level (or denominator) is zero before running calculations?
**Answer:** Checking before running calculations prevents a `ZeroDivisionError`, which would immediately crash the program and interrupt automated operations. Implementing defensive checks ensures the Digital Twin system handles edge cases—such as empty fuel tanks or missing telemetry data—gracefully without halting execution.

### Q2: Why are lists and `for` loops useful when automating repetitive farm tasks?
**Answer:** Lists store collections of operational data (like field coordinates or machinery status) in a structured format, while `for` loops allow automated iteration over every item. This eliminates manual code repetition, scales easily as farming operations expand, and guarantees consistent data execution across all fields.

### Q3: Why use dictionaries or sets instead of standard lists for specific farm data?
**Answer:** Dictionaries provide fast O(1) key-value lookups, making them ideal for retrieving specific metadata (e.g., mapping a specific tractor ID to its status). Sets enforce uniqueness automatically, which is essential when tracking distinct list items like unique crop varieties or field locations without handling manual duplicates.

---

## Visual Evidence
*(Uploaded project screenshots capturing core execution logic and code outputs reside in the `/images` directory.)*
