# MediStock – Real-Time Hospital Inventory Tracker

**MediStock** is a Java-based inventory management system designed for healthcare providers. It integrates real-world CMS (Medicare/Medicaid) data to track medication stock levels, expiration dates, and reimbursement logic.

## 🚀 Project Impact
- **Core Competencies:** Java, Object-Oriented Programming (OOP), SQLite/JDBC, HIPAA-Compliant Audit Logging, Medicare/Medicaid Reimbursement Modeling.
- **Objective:** Provide a HIPAA-compliant inventory and financial analytics engine for pharmacy informatics and healthcare supply chain analysts.

## 🛠️ Technical Stack
- **Language:** Java 17+
- **Build & Dependency Management:** Apache Maven (with bundled Maven Wrapper)
- **Database & Persistence:** SQLite & JDBC
- **Libraries:** OpenCSV, SLF4J, JUnit 5
- **Data Visualization:** Tableau Public
- **Data Source:** CMS.gov Medicare Part D Prescriber & ASP Pricing Data

## 📅 Development Milestones

### Week 1: Foundation & Data Ingestion (COMPLETED)
- [x] **Core OOP Architecture:** Implemented `InventoryItem` parent class with `Medication` and `MedicalDevice` inheritance.
- [x] **Maven Integration:** Configured project structure and dependencies using Maven.
- [x] **Data Parsing:** Integrated **OpenCSV** to ingest large-scale CMS Medicare datasets.
- [x] **Data Mapping:** Built `DataMapper` to sanitize raw CSV strings and map them into domain objects.
- [x] **Inventory Manager:** Developed a `HashMap`-based lookup engine for $O(1)$ inventory access.
- [x] **Console UI:** Built an interactive command-line interface for data ingestion and reporting.

### Week 2: Intelligent Monitoring, Persistence & Financial Logic (COMPLETED)
- [x] **Expiration Engine:** Implemented `PriorityQueue` for $O(1)$ access to the most urgent expiring medications.
- [x] **Observer Pattern:** Built a decoupled notification system (`StockNotifier`) with Email and SMS alert observers.
- [x] **Automated Alerts:** Integrated low-stock triggers that broadcast alerts across registered observers.
- [x] **CMS Reimbursement Logic:** Implemented calculations for **Medicare Part B (ASP + 6%)** and **340B Drug Pricing**.
- [x] **Database & HIPAA Audit Logging:** Added SQLite persistence via `InventoryDAO` and sanitized access tracking via `SecurityLogger`.
- [x] **Unit Testing:** Verified financial calculations and alert thresholds using **JUnit 5**.

## 📊 Data Visualization & Analytics
MediStock exports processed inventory and financial risk metrics for executive oversight.

### Interactive Dashboard
[👉 View MediStock Executive Dashboard on Tableau Public](https://public.tableau.com/views/MediStock_Executive_Dashboard/Dashboard1)

**Key Metrics Tracked:**
- **Real-Time Stock Levels:** Categorized by Red-Green urgency thresholds.
- **Financial Risk Exposure:** Identification of high-cost inventory nearing expiration.
- **Reimbursement Potential:** Projected Medicare Part B and 340B payouts based on active stock.

## 💻 Installation & How to Run

### Prerequisites
- **Java Development Kit (JDK):** Version 17 or higher
- **Git** *(Maven is bundled via Maven Wrapper—no separate Maven installation required)*

### Option 1: Run via Command Line / Terminal (Recommended)

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Bricebazo/MediStock-Hospital-Inventory.git](https://github.com/Bricebazo/MediStock-Hospital-Inventory.git)
   cd MediStock-Hospital-Inventory