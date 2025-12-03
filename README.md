# 📊 ETL & BPMN — Consolidated Case Studies 

This repository contains **all ETL modeling tasks**, including classic warehouse design scenarios and the **PUCIT dual-server integration**. Each task includes sources, transformations, and target warehouse tables.

---

## ✅ Objective 1 — Basic ETL Modeling  
**Source:** Category, Product, Supplier  
**Target:** DimProduct, DimSupplier, FactInventory  
**ETL Summary:** Standard extraction → join Product with Category/Supplier → clean → load dims + fact.

---

## ✅ Objective 2 — Multi-Source Integration  
**Additions:** CategoryName and Supplier.City  
**Target:** Enhanced DimProduct, DimSupplier, FactInventory  
**ETL Summary:** Join tables, derive fields, compute DefectRate, load DW.

---

## ✅ Objective 3 — Technical Architecture (3 Stores)  
**Sources:** Lahore, Islamabad, Peshawar  
**ETL Summary:** Extract from 3 servers → add StoreID → unify → clean → load centralized DW.

---

## ✅ Objective 4 — User Entity Modeling  
**Sources:** Product, Supplier, ProductManager categories, Investor ratings  
**DW:** DimCategory, DimProductRating, DimProduct, DimSupplier, FactInventory  
**ETL Summary:** Derive Category (New/Established/Old), average ProductRating, assign CityPriority, load DW.

---

## ✅ Objective 5 — Business Entity Integration  
**Sources:** Inventory, Sales, Customers, Feedback, Loyalty  
**DW:** DimProduct, DimCategory, DimSupplier, DimTime, FactInventory  
**ETL Summary:** Extract all entities → build dimensions → compute StockValue → load FactInventory.

---

## ✅ Objective 6 — PUCIT Centralized Data Warehouse (Dual Servers)
### **Source Servers**
**Server A (Old Campus):**  
- Students.xlsx  
- Faculty.db  
- Attendance.csv  

**Server B (New Campus):**  
- Students.csv  
- Faculty.json  
- Attendance.xlsx  

### **DW Targets**
- **DW_Students**  
- **DW_Faculty**  
- **DW_Attendance**

### **ETL Summary**
- Extract Excel/CSV/JSON/SQLite  
- Standardize fields + normalize dates  
- Add `CampusID` (A/B)  
- Merge student/faculty/attendance from both servers  
- Resolve duplicates + missing values  
- Load unified DW tables
