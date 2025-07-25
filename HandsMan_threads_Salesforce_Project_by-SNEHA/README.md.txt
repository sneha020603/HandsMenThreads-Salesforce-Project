# 🧵 HandsMen Threads – Salesforce Automation Project

> 👩‍💻 Developed by **Sneha Kumari** | 🎓 LNCT Bhopal | ☁️ Salesforce Dev Org: `snehakri0206875@agentforce.com`

---

## 📌 Project Overview

**HandsMen Threads** is a Salesforce-powered business automation solution designed for managing a clothing & accessories brand. The project integrates various Salesforce tools like:

- **Record-Triggered Flows**
- **Email Alerts**
- **Loyalty Program logic (via Flow/Formula)**
- **Inventory Stock Alerts**
- **Scheduled Batch Job**
- **Custom Object Modeling & Relationships**

---

## 🛠️ Features Implemented

### 1. 📧 Order Confirmation Email
- Record-Triggered Flow on `Order__c`
- Trigger: When `Status__c = Confirmed`
- Action: Send Email Alert using `Order Confirmation Email Template`

### 2. 🎁 Loyalty Program
- Logic implemented via Flow + Criteria:
  - Customers with more than 3 orders → Status: `Gold`
  - Auto Email sent with Discount Coupon

### 3. ⚠️ Inventory Stock Alerts
- Condition: `Stock_Quantity__c < Threshold`
- Sends Alert Email to Manager
- Updates `Low_Stock__c = TRUE`

### 4. 🔁 Batch Update Jobs
- Schedule batch to update Loyalty Levels every month
- Checks total orders and updates `Loyalty_Status__c`

### 5. 🌐 Lightning App Page
- Using Lightning App Builder
- Components:
  - Order Record Page
  - Loyalty Status Card
  - Inventory Alert Panel

---

## 🧩 Custom Data Model (Schema)

### Objects Created:
- `Order__c`
- `Customer__c`
- `Product__c`
- `Inventory__c`
- `Loyalty_Record__c`

> 📌 Relationships:
> - Order__c → Lookup to Customer__c
> - Order__c → Master-Detail to Product__c
> - Inventory__c → Lookup to Product__c

---

## 📊 ER Diagram
See `ER_Diagram_HandsMenThreads.png` for full schema overview.

---

## 📷 Screenshots (Add as needed)
- {fig1: Flow Setup for Order Confirmation}
- {fig2: Email Alert Setup}
- {fig3: Loyalty Logic Criteria}
- {fig4: Inventory Threshold Trigger}
- {fig5: Scheduled Job in Apex (placeholder)}

---

## 📁 Folder Structure
```
HandsMenThreads_Salesforce_Project/
├── Project_Report_SnehaKumari_LNCT.docx
├── ER_Diagram_HandsMenThreads.png
├── Screenshots/
├── README.md
```

---

## 🚀 How to Deploy
1. Setup Dev Org or Scratch Org
2. Create custom objects as per schema
3. Setup Flows from screenshots
4. Create email alerts & templates
5. Deploy batch classes using VS Code + SFDX

---

## 👩‍🎓 Developer Info
- 👩‍💻 **Sneha Kumari**
- 🎓 LNCT Bhopal | CSE (IoT & Cybersecurity)
- 📬 Email: snehakri0206@gmail.com


---

## 📜 License
This project is free to use for academic and learning purposes.

---
