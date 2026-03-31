
---

```markdown
# Invasive Species Data Entry Dashboard

A Shiny-based desktop application for logging invasive species removal data, tracking effort metrics, and generating automated summaries.

## 📁 Project Structure
The project is organized to keep scripts and data separate for easy management:
* **`Invasive_Data_Entry.R`**: The main application script (located in the root).
* **`Data/`**: A subdirectory created automatically to store the database.
* **`Data/invasive_species_data.xlsx`**: The persistent Excel database containing raw logs and summaries.

## 🛠 Prerequisites
Ensure you have **R** and **RStudio** installed. You will need the following packages:
```r
install.packages(c("shiny", "openxlsx"))
```

## Getting Started
1. **Open the Project**: Open `Invasive_Data_Entry.R` in RStudio.
2. **Set Working Directory**: Ensure the `setwd()` path matches your local folder.
3. **Run**: Click **Run App** in the top right of the editor.

## Data Entry Rules
* **Validation**: The app requires **# of Bags** to be greater than 0. If set to 0, the app will display an error and block the submission to prevent incomplete data logs.
* **Smart Fields**: After a successful submission, the "Site" remains selected to allow for rapid multi-entry at the same location, while effort and species fields reset to defaults.
* **Undo**: The **Remove Last Entry** button will delete the most recent row from the session and the Excel file.

## Data & Summaries
The app maintains a single Excel workbook with three automated tabs:
1. **Data**: Raw entry logs.
2. **Monthly_Summary**: Totals for people, acres, bags, and time grouped by month.
3. **Quarterly_Summary**: Totals grouped by fiscal quarter.

> **Note**: Always close the Excel file before clicking "Submit" in the app, or the save will fail due to a file-lock error.

```

---


