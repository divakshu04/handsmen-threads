# 👔 HandsMen Threads: Elevating the Art of Sophistication in Men's Fashion

## 📌 Project Overview

**HandsMen Threads** is a modern fashion brand aiming to revolutionize its operations through **Salesforce CRM**. This project enhances customer experience and internal operations by automating order confirmations, dynamic loyalty programs, proactive stock alerts, and scheduled order processing.

The Salesforce implementation includes robust **data modeling**, **data quality enforcement**, **automated workflows**, **Apex triggers**, and **asynchronous batch processing**, ensuring the system is scalable, secure, and business-efficient.

---

## 🎯 Key Features

- **📦 Custom Object Model**: Tailored objects for Customers, Orders, Products, Inventory, and Campaigns.
- **📬 Email Automation**:
  - Order Confirmations
  - Loyalty Program Updates
  - Low Stock Alerts
- **🔁 Automated Flows**:
  - Triggered flows based on order and inventory status
  - Scheduled loyalty updates
- **🧠 Apex Triggers & Batch Jobs**:
  - Auto-calculation of order totals and loyalty points
  - Daily inventory sync with external systems
- **🔐 Robust Data Security**:
  - Custom roles and profiles for access control
  - Role-based data access to Sales, Inventory, and Marketing teams

---

## 🧱 Project Structure

### 🗂️ Custom Objects

| Object Name            | Purpose                              |
|------------------------|--------------------------------------|
| `HandsMen_Customer__c` | Stores customer details              |
| `HandsMen_Order__c`    | Manages order transactions           |
| `HandsMen_Product__c`  | Holds product information            |
| `Inventory__c`         | Tracks stock levels and warehouse    |
| `Marketing_Campaign__c`| Manages marketing initiatives        |

### 🔐 Data Security Roles

| Role              | Access Permissions                              |
|------------------|--------------------------------------------------|
| Sales Manager     | Full Access to Customers and Orders             |
| Inventory Manager | Read/Edit Inventory & Products                  |
| Marketing Team    | Read Customers, Edit Campaigns                  |

---

## ⚙️ Automation & Logic

### ✅ Email Templates

| Template Name         | Format | Trigger Condition                              |
|-----------------------|--------|-----------------------------------------------|
| Order Confirmation    | HTML   | When order is confirmed                        |
| Low Stock Alert       | Text   | When stock quantity < 5                        |
| Loyalty Program Email | HTML   | When customer qualifies for loyalty upgrade    |

### 🔁 Record-Triggered Flows

| Flow Name                 | Trigger Condition                            |
|--------------------------|----------------------------------------------|
| Order Confirmation Flow  | `Order__c.Status__c == 'Confirmed'`          |
| Stock Alert Flow         | `Inventory__c.Stock_Quantity__c < 5`         |
| Loyalty Status Flow      | Scheduled Daily Flow                         |

### 🧠 Apex Triggers

| Trigger Name            | Object           | Purpose                                      |
|-------------------------|------------------|----------------------------------------------|
| Update Order Total      | Order__c         | Auto-calculate total on order save           |
| Stock Deduction         | Inventory__c     | Decrease stock when an order is placed       |
| Loyalty Status Update   | Customer__c      | Update loyalty based on purchase history     |

### ⏱️ Batch Jobs

| Job Name                 | Purpose                                     | Schedule              |
|--------------------------|---------------------------------------------|------------------------|
| Loyalty Points Calculation | Weekly points update                      | Every Sunday 12 AM     |
| Inventory Sync            | Sync with external warehouse system        | Daily at 2 AM          |

---

## 🛠️ Tools & Technologies

- **Salesforce Platform**
- **Salesforce Flow Builder**
- **Apex / Apex Triggers**
- **Asynchronous Apex (Batch Jobs)**
- **Validation Rules**
- **Security Roles and Profiles**
- **Lightning App Builder**

---

## 📚 What I Learned

- Designing complex **data models** in Salesforce
- Enforcing **data integrity** with validation rules
- Building **record-triggered** and **scheduled flows**
- Writing **Apex logic** to handle business-specific processes
- Managing **batch jobs** for asynchronous processing
- Securing data using **roles, profiles, and sharing rules**

---

## 📂 Metadata Structure

Important metadata was retrieved using Salesforce CLI and is organized under:

force-app/
└── main/
    └── default/
        ├── objects/
        ├── classes/
        ├── triggers/
        ├── flows/
        ├── layouts/
        ├── profiles/
        └── email/


📽️ **[Click here to watch the demo video](https://drive.google.com/file/d/1ke3ElNlMFDCw2ti5cob9mrmOp20mVMEb/view?usp=sharing)**  
📄 **[Click here to read the full project report](https://drive.google.com/file/d/1aCKTyFdJVwfzDW49wc4K_GAqvHPQ5Mfm/view?usp=sharing)**

---

## 🚀 How to Explore the Project

1. Clone the repo in VS Code
2. Authenticate to your Salesforce org
3. Use **Org Browser: Focus on Metaddata View** or `SFDX: Deploy Source to Org`
5. Use **App Launcher** to open "HandsMen Threads"
6. Place test orders and simulate stock drop to see automation

---

## 🙋‍♂️ Author

**Divakshu Sharma**  
📧 divakshusharma@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/divakshu-sharma/)

