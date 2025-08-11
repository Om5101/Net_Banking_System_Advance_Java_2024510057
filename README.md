# 🏦 Banking Management System

A **Java-based web application** that simulates a real-world **banking platform** with separate roles for **Customers** and **Admins**.  
It allows customers to create accounts, perform secure transactions, and request checkbooks, while admins can approve accounts and manage requests.  

This project was built as part of my academic learning to strengthen **Java, JDBC, MySQL, and MVC architecture** skills and to demonstrate my ability to design a **complete full-stack application**.

---

## 🎯 Objective

The goal was to create a **secure, role-based banking system** that:
- Demonstrates **end-to-end banking workflows** (Account creation → Login → Transactions → Requests → Admin approvals)
- Uses **proper software engineering practices** like **MVC architecture**, **UML diagrams**, and **modular coding**
- Follows **real-world constraints** such as account approval before login, transaction validation, and balance checks.

---

## 📌 Problem Statement

In real banks, customers cannot directly perform transactions without:
1. **Creating an account**  
2. **Getting approval** from bank staff  
3. **Ensuring sufficient balance** for transactions  

My system replicates this workflow in a **simplified, educational model**:
- Customer → creates account → waits for admin approval  
- Customer → logs in → views balance/transactions → sends money  
- Admin → reviews pending requests → approves/rejects  

---

## 🚀 Features

### 👤 Customer
- **Create Bank Account** – Registers with basic details (status set to `inactive` until approved)
- **Login to NetBanking** – Validates credentials and checks if account is approved
- **View Account Balance** – Fetches latest balance from database
- **View Transaction History** – Shows debit/credit history
- **Send Money** – Validates receiver account, checks sender balance, updates both accounts atomically
- **Apply for Checkbook** – Sends request for admin approval

### 🛠️ Admin
- **Login to Admin Dashboard**
- **View Pending Accounts** – See list of accounts awaiting approval
- **Approve / Reject New Accounts**
- **Approve / Reject Checkbook Requests**

---

## 🏗️ Tech Stack

| Layer        | Technology Used |
|--------------|-----------------|
| **Frontend** | JSP, HTML, CSS  |
| **Backend**  | Java Servlets (MVC Pattern) |
| **Database** | MySQL |
| **Server**   | Apache Tomcat |
| **Languages**| Java, SQL, HTML, CSS |

---

## 📂 Project Structure



