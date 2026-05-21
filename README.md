# Secure-Quest-DataBase_Project
A secure local web application featuring a PHP/MySQL backend API and a frontend that supports question encryption. Includes role-based access for Teachers (creation) and Exam Incharges (approval/rejection).

A Full-Stack Secure Question Paper Generation Portal with End-to-End Encryption.

---

## 📌 Project Overview
**Secure Quest** is a secure local web application designed to digitize and secure the process of exam paper generation. The system ensures top-tier security and privacy by allowing teachers to encrypt questions before submitting them. It features a complete role-based workflow between **Teachers** (who create the paper) and the **Exam Incharge** (who reviews, approves, or rejects the paper).

## 🚀 Key Features
* **Role-Based Dashboards:** Separate panels and access controls for Teachers and the Exam Incharge.
* **Question-Level Encryption:** Teachers input questions one by one, which are encrypted on the client side before hitting the network/database.
* **Approval Workflow:** The Exam Incharge receives the generated papers and has the authority to either **Approve** or **Reject** them.
* **Secure API Backend:** Built using PHP to handle business logic and securely communicate with the database.
* **Robust Data Storage:** MySQL database configured to store user roles, logs, and encrypted question payloads.

---

## 🛠️ Tech Stack
* **Frontend:** HTML5, CSS3, JavaScript (ES6)
* **Backend:** PHP (API-driven architecture)
* **Database:** MySQL
* **Security/Cryptography:** Client-side JavaScript Encryption (e.g., AES/CryptoJS)

---

## ⚙️ System Architecture & Workflow
1.  **Authentication:** Users log in using their credentials (Teacher / Exam Incharge).
2.  **Paper Creation (Teacher):** The teacher drafts the question paper. Each question is encrypted using a cryptographic algorithm via JavaScript.
3.  **Data Transmission:** The encrypted questions are sent via PHP APIs to the backend server.
4.  **Storage:** The PHP backend stores the encrypted strings into the MySQL database.
5.  **Review & Action (Incharge):** The Exam Incharge fetches the pending papers, decodes/reviews them, and updates the status to either *Approved* or *Rejected*.

---

## 💻 How to Run Locally

### Prerequisites
* XAMPP installed.
* Web Browser (Chrome, Firefox, Edge, etc.)
* Git (Optional)

### Installation Steps
1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/IfzaRizwan98/Secure-Quest-DataBase_Project.git](https://github.com/IfzaRizwan98/Secure-Quest-DataBase_Project.git)
    ```
2.  **Setup Backend & Database:**
    * Move the project folder to your local server directory (e.g., `C:/xampp/htdocs/` or `/var/www/html/`).
    * Open **phpMyAdmin** (`http://localhost/phpmyadmin`).
    * Create a new database (e.g., `secure_quest_db`).
    * Import the `.sql` backup file provided in the repository.
3.  **Configure Database Connection:**
    * Open the database configuration file in the PHP directory.
    * Update the database name, username, and password according to your local environment.
4.  **Run the Application:**
    * Start Apache and MySQL modules in your XAMPP/WAMP control panel.
    * Open your browser and navigate to: `http://localhost/Secure-Quest-DataBase_Project/`

---

## 🛡️ Security Implementations
* **Client-Side Encryption:** Protects against SQL Injection and sniffing attacks during data transmission.
* **Secure APIs:** PHP APIs handle queries using prepared statements to prevent unauthorized data tampering.

---
