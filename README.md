# 🏦 Banking Management System

A **Java-based web application** built as part of our **Advanced Java** university coursework (semester-long group project).  
The system provides **banking operations for customers** and **administrative functionalities for bank staff**, with role-based access, secure transactions, and an intuitive JSP/Servlet UI.

---

## 📸 Project Walkthrough – Screenshots

The following screenshots take you through the key flows of the **Banking Management System** from both **User** and **Admin** perspectives.  

---

### 📝 Step 1: New User Opens an Account
Our journey begins when a new customer fills out the **Online Account Opening Form**.  
They provide all necessary personal and banking details to initiate their account request.

**User_Create_Account**  
<img width="1351" height="838" alt="User_Create_Account" src="https://github.com/user-attachments/assets/3fad6493-8181-42fd-ac53-51010765c8d3" />

---

### 🛠 Step 2: Bank Admin Reviews and Manages Accounts
Once the request is submitted, the **Bank Admin** logs into their secure dashboard to process it.

**Admin_Login** – The admin signs in to access the control panel.  
<img width="1354" height="603" alt="Admin_Login" src="https://github.com/user-attachments/assets/de31c11e-60be-438e-82d2-355512123276" />

**Admin_NewAccountRequestStatus** – Admin views pending account opening requests for approval or rejection.  
<img width="1241" height="514" alt="Admin_NewAccountRequestStatus" src="https://github.com/user-attachments/assets/c0136fbd-7dfe-4ce7-8fff-07dadd523d15" />

**Admin_ViewAllAccounts** – Full list of all active and pending accounts in the bank’s database.  
<img width="1225" height="944" alt="Admin_ViewAllAccounts" src="https://github.com/user-attachments/assets/93d3d77c-ea01-4d78-82b1-83a803562931" />

**Admin_VeiwAllTransactions** – Overview of every transaction recorded in the system.  
<img width="1226" height="784" alt="Admin_VeiwAllTransactions" src="https://github.com/user-attachments/assets/f22468ef-a2e4-4fed-9a44-085810e49f55" />

**Admin_Level_Transactions** – Drill-down into transaction details at a specific account level.  
<img width="1243" height="654" alt="Admin_Level_Transactions" src="https://github.com/user-attachments/assets/24af1752-fa79-472c-b766-fd4bacf4f868" />

**Admin_AllChequeRequestStatus** – Status list of all customer cheque book requests.  
<img width="1224" height="649" alt="Admin_AllChequeRequestStatus" src="https://github.com/user-attachments/assets/07e28087-bc8c-4c19-b357-db314bf453b8" />

**Admin_OpenNewAccount** – Admin can also create a customer account directly.  
<img width="1227" height="736" alt="Admin_OpenNewAccount" src="https://github.com/user-attachments/assets/1dd1df95-02fa-4ce1-9ee8-3f6f7640e031" />

---

### 👤 Step 3: Bank User Accesses Services
Once approved, the customer logs in and can use various banking features.

**User_ViewProfile** – Customer can view their personal and account details.  
<img width="1224" height="692" alt="User_ViewProfile" src="https://github.com/user-attachments/assets/4cccce03-63dd-425c-8b48-1de1f0c60d65" />

**User_SendMoney** – Transfer money to another account quickly and securely.  
<img width="1225" height="626" alt="User_SendMoney" src="https://github.com/user-attachments/assets/d7f12baf-5dc7-4992-b90e-172e109a3849" />

**User_ViewAllTransactions** – Access the entire history of past transactions.  
<img width="1223" height="493" alt="User_ViewAllTransactions" src="https://github.com/user-attachments/assets/3f76c5ad-124b-4615-8648-1a264ad9bca8" />

**User_BalanceCheckFeature** – Instantly check the account balance.  
<img width="1246" height="278" alt="User_BalanceCheckFeature" src="https://github.com/user-attachments/assets/2e3c1fb4-6feb-4f41-b65e-6d2f53886ef8" />

**User_ApplyCheque** – Request a cheque book online without visiting the branch.  
<img width="1246" height="390" alt="User_ApplyCheque" src="https://github.com/user-attachments/assets/1e374d42-c070-474d-a190-592a86c2bd7e" />

**User_ChangePassword** – Securely update login credentials anytime.  
<img width="1224" height="626" alt="User_ChangePassword" src="https://github.com/user-attachments/assets/6002ffc7-0c71-433b-be5c-93295e5a6590" />

---

💡 **This flow ensures a seamless digital banking experience** — from account creation to everyday transactions — with clear separation of **User** and **Admin** roles.















## 📌 Features

### 👤 User Features
- Create a new bank account
- Login/Logout with session management
- View account balance and transaction history
- Apply for a checkbook
- Transfer money between accounts
- Change or reset password
- Access netbanking services

### 🛠 Admin Features
- Create and manage customer accounts
- Approve or reject account and transaction requests
- Credit/Debit customer accounts
- Search and view account details
- Manage transaction records
- View all users and their statuses

---

## 🏗 Tech Stack
- **Java EE (Servlets & JSP)**
- **JDBC** for database connectivity
- **MySQL** as the database
- **Maven** for build and dependency management
- **JSTL** for dynamic JSP rendering
- **HTML, CSS, JavaScript** for UI
- **NetBeans IDE** for development
- **Tomcat Server** for deployment

---

## 📂 Project Structure

## 🚀 How to Run Locally

### 1️⃣ Prerequisites
- **Java JDK 8+**
- **Apache Tomcat 9+**
- **MySQL Server**
- **Maven**
- **NetBeans IDE** (or any IDE with Java EE support)
