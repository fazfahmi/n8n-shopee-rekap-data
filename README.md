# 📊 n8n Workflow – Shopee Stores Data Pipeline

## 📝 Description
This workflow was built in **n8n** to automate reporting for multiple Shopee stores.  

Currently, Shopee's APIs are not directly connected, so the workflow processes **exported files** (Orders, Balance, and Internal Ads) that are manually downloaded and placed in a **Google Drive folder**.  

Each store has its own folder, and the workflow automatically sorts and sends the data into the correct **Google Sheets** (e.g., Internal Ads – Store A, Internal Ads – Store B).

---

## ⚙️ Workflow Steps
1. **Schedule Trigger**  
   - Runs on a daily schedule.  

2. **Google Drive Node**  
   - Monitors a specific folder that contains downloaded Shopee reports.  
   - Files are organized by store name.  

3. **Filter by Filename**  
   - Detects whether the file is: Orders, Balance, or Internal Ads.  
   - Identifies which store the file belongs to (e.g., Store A, Store B).  

4. **Google Sheets Node**  
   - Uploads the parsed data into the correct sheet, e.g.:  
     - *Internal Ads – Store A*  
     - *Orders – Store B*  
     - *Balance – Store C*  

---

## 🖼️ Workflow Example
Below is a simplified view of how the workflow is structured in n8n:

<img width="1002" height="677" alt="image" src="https://github.com/user-attachments/assets/4dea98fb-cc0f-40d6-8dbd-95b12b8cc3ab" />

---

## 🚀 Implementation Results
- Centralized reporting across multiple Shopee stores.  
- No need to manually copy-paste CSV/Excel into spreadsheets.  
- Each file is automatically sorted and stored in the right Google Sheet.  
- Saves ~2–3 hours of manual reporting per day.  

---

## ⚠️ Notes
- This workflow uses **dummy credentials and dummy file paths** in the exported JSON.  
- The real version runs internally with actual Shopee data.  

---
