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

Banking-App/
│
├── src/
│   ├── main/
│   │   ├── java/                                   # Java source code
│   │   │
│   │   │   ├── com.admin.servlet/                  # Servlets for Admin functionalities
│   │   │   │   ├── AddTransaction.java             // Admin adds new transactions
│   │   │   │   ├── ApproveStatus.java              // Approve account or transaction requests
│   │   │   │   ├── CreateAccnt.java                // Create new customer account (Admin)
│   │   │   │   ├── EditServlet.java                // Edit account details (Admin)
│   │   │   │   ├── EditViewServlet.java            // Fetch account details for editing
│   │   │   │   ├── RejectServlet.java              // Reject pending applications
│   │   │   │   ├── SearchAccount.java              // Search account details
│   │   │   │   ├── SerchAccnt.java                 // (Typo) Similar to SearchAccount
│   │   │   │   ├── SerchTransaction.java           // (Typo) Search transactions
│   │   │   │   ├── ViewAccnt.java                  // View account summary
│   │   │
│   │   │   ├── com.dao/                            # Data Access Objects
│   │   │   │   ├── AdminDAO.java                   // Interface for Admin DB operations
│   │   │   │   ├── AdminDAOImpl.java               // Implementation of Admin DAO
│   │   │   │   ├── CheckDAO.java                   // Interface for Check DB operations
│   │   │   │   ├── UserDAO.java                    // Interface for User DB operations
│   │   │   │   ├── UserDAOImpl.java                // Implementation of User DAO
│   │   │
│   │   │   ├── com.db/                             # Database utilities
│   │   │   │   ├── DbConnect.java                  // Establish database connection
│   │   │
│   │   │   ├── com.entity/                         # Entity / Model classes
│   │   │   │   ├── AccountTransaction.java         // Represents transaction entity
│   │   │   │   ├── ApplyCheck.java                 // Represents checkbook application
│   │   │   │   ├── User.java                       // Represents User entity
│   │   │
│   │   │   ├── com.user.servlet/                   # Servlets for User functionalities
│   │   │       ├── ApplyCheckServlet.java          // Apply for a checkbook
│   │   │       ├── create_account_servlet.java     // Create account (User)
│   │   │       ├── ForgotPassword.java             // Handle forgot password
│   │   │       ├── LoginServlet.java               // Handle user login
│   │   │       ├── LogoutServlet.java              // Handle user logout
│   │   │       ├── NetbankingServlet.java          // Handle netbanking features
│   │   │       ├── PasswordChange.java             // Change password
│   │   │       ├── SendMoneyServlet.java           // Transfer money between accounts
│   │
│   │   ├── resources/                              # App configuration files (empty here)
│
│   ├── webapp/                                     # Frontend files (JSP, CSS, JS, Images)
│   │   ├── admin/                                  # Admin panel JSP pages
│   │   │   ├── acc_status.jsp                      // Show account status
│   │   │   ├── all_trans.jsp                       // Show all transactions
│   │   │   ├── all_user.jsp                        // Show all users
│   │   │   ├── allcss.jsp                          // CSS for admin pages
│   │   │   ├── check_status.jsp                    // Show check request status
│   │   │   ├── edit_acc.jsp                        // Edit account form
│   │   │   ├── index.jsp                           // Admin dashboard home
│   │   │   ├── left-navbar.jsp                     // Sidebar navigation
│   │   │   ├── main_navbar.jsp                     // Top navigation bar
│   │   │   ├── myjs.jsp                            // JS scripts for admin
│   │   │   ├── new_transaction.jsp                 // Form to create new transaction
│   │   │   ├── open_acc.jsp                        // Open new account
│   │   │   ├── serch_trans.jsp                     // Search transaction
│   │   │   ├── style.css                           // Admin page styles
│   │   │   ├── view_profile.jsp                    // View admin profile
│   │
│   │   ├── all_component/                          # Common reusable UI components
│   │   │   ├── allCss_file.jsp                     // Common CSS import
│   │   │   ├── footer.jsp                          // Footer component
│   │   │   ├── navbar.jsp                          // Navbar component
│   │   │   ├── style.css                           // Common styles
│   │
│   │   ├── img/                                    # Image resources
│   │
│   │   ├── js/                                     # JavaScript files
│   │   │   ├── myjs.js                             // Common JS functions
│   │   │   ├── script.js                           // Validation and UI scripts
│   │
│   │   ├── META-INF/
│   │   │   ├── context.xml                         // Context configuration
│   │
│   │   ├── WEB-INF/                                # Secured JSPs & Config
│   │   │   ├── web.xml                             // Deployment descriptor
│   │   │   ├── all_transaction.jsp                 // Show all transactions (secure)
│   │   │   ├── apply_check.jsp                     // Apply for checkbook (secure)
│   │   │   ├── balance.jsp                         // Show account balance
│   │   │   ├── chngpswd.jsp                        // Change password
│   │   │   ├── create_account.jsp                   // Account creation form
│   │   │   ├── credit.jsp                           // Credit money
│   │   │   ├── debit.jsp                            // Debit money
│   │   │   ├── forgot.jsp                           // Forgot password form
│   │   │   ├── home.jsp                             // User home dashboard
│   │   │   ├── index.jsp                            // Landing page
│   │   │   ├── login.jsp                            // Login form
│   │   │   ├── netbanking.jsp                       // Netbanking page
│   │   │   ├── send_money.jsp                       // Money transfer form
│   │   │   ├── viewprofile.jsp                      // View user profile
|
├── target/                                          # Maven build output directory
│
├── nb-configuration.xml                             # NetBeans project-specific configuration
│
└── pom.xml                                          # Maven build configuration (dependencies, plugins)




