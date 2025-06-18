# ProjectTalend   
A data integration and transformation project using **Talend Open Studio**, demonstrating real-world ETL workflows across multi-format datasets, legacy mainframe files, multilingual surveys, and cloud data warehousing with Snowflake.

---

## 📁 Project Structure

### 🔹 Assignment 1: Load Customer Data to Snowflake
**Goal:** Ingest cleaned customer data into the **Snowflake Cloud Data Warehouse** for analytics.

**Tasks:**
- Read CSV data using `tFileInputDelimited`
- Clean and transform using `tMap` 
- Load data into target table using `tSnowflakeOutput`
- Handle batch commits, data typing, and nulls

---

### 🔹 Assignment 2: Convert and Integrate Multi-Format Data Sources  
**Goal:** Merge product data from XML, JSON, and Excel into a unified report.

**Tasks:**
- Flatten `orders.xml` using `tFileInputXML`
- Extract fields from `products.json` with `tFileInputJSON`
- Clean `inventory.xlsx` using `tFileInputExcel`
- Join all sources on `product_id` via `tMap`
- Output results as both CSV and JSON

---

### 🔹 Assignment 3: Legacy Mainframe File Conversion with Data Enrichment  
**Goal:** Parse an EBCDIC-encoded file using a COBOL copybook and enrich it with account balances.

**Tasks:**
- Read `customer_data.ebc` using `tFileInputPositional` + `cobol.cpy`
- Clean account fields and standardize names
- Join with account balance CSV using `tMap`
- Add `Account_Status = ACTIVE / INACTIVE` based on balance
- Export enriched data to JSON using `tFileOutputJSON`

---

### 🔹 Assignment 4: Multilingual Survey Data Integration and Format Transformation  
**Goal:** Consolidate survey data from Asia, Europe, and Africa across Excel, JSON, and XML formats.

**Tasks:**
- Ingest:
  - `survey_asia.xlsx` (Unicode + regional dates)
  - `survey_europe.json` (Nested JSON, ISO dates)
  - `survey_africa.xml` (Localized XML structure)
- Flatten and standardize all datasets using `tMap`
- Export unified data to both CSV and Excel formats

---

## 🛠️ Tools & Components Used

- **Talend Open Studio**
- **Snowflake Cloud Warehouse**
- `tFileInputDelimited`, `tFileInputXML`, `tFileInputExcel`, `tFileInputJSON`, `tFileInputPositional`, `tMap`
- `tSnowflakeInput`, `tSnowflakeOutput`
- `tFileOutputJSON`, `tFileOutputDelimited`, `tFileOutputExcel`
- Rejected row handling, conditional logic, and logging

---

## 📌 Key Concepts Learned

- Multi-format data parsing and flattening (XML, JSON, Excel)
- COBOL copybook integration for legacy data
- Survey data normalization across regions and languages
- Real-time transformation and conditional fields using `tMap`
- Secure data loading to Snowflake cloud platform
- Output generation in CSV, Excel, and JSON formats

---

## 📤 Outputs

- Unified product reports (CSV & JSON)
- Enriched customer records (JSON)
- Consolidated multilingual surveys (CSV & Excel)
- Cleaned Snowflake-ready datasets

---

## 👩‍💻 Author

**Lasya Reddy**  

---

## ⭐️ How to Use

1. Clone the repo and open in **Talend Open Studio**  
2. Configure file paths and credentials (especially for Snowflake)  
3. Run each job from the workspace based on its assignment folder  
4. Check the output folder or Snowflake for results
