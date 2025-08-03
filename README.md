# 📚 Student Database CRUD Application (Java + JDBC + MVC)

This project is a **console-based Java application** that demonstrates the implementation of **CRUD operations** (Create, Read, Update, Delete) on a **MySQL database** using **JDBC** and follows the **MVC (Model-View-Controller)** design pattern.

---

## 🔧 Technologies Used

- **Java SE**
- **JDBC (Java Database Connectivity)**
- **MySQL**
- **MVC Architecture**
- **Git & GitHub**

---

## 🧱 Project Structure

learn_jdbc/
├── model.java # Database logic (Model)
├── View.java # Input/output interface (View)
├── controller.java # Application control flow (Controller)
└── Main.java # Entry point (to be added by user)




---

## 🧠 How It Works

### ✅ Model
Handles all the **database operations** using JDBC:
- `insert()` - Adds a new student
- `select()` - Fetches a student by roll number
- `update()` - Updates student name
- `delete()` - Deletes a student record

### ✅ View
Handles **user interaction**:
- Displays menu
- Accepts user input
- Prints success/error messages

### ✅ Controller
Acts as the **application brain**:
- Gets input from View
- Calls Model functions
- Sends response back to View

---

## ▶️ How to Run

1. **Set up MySQL Table:**

```sql
CREATE DATABASE student_db;

USE student_db;

CREATE TABLE STUDENT (
    ROLL INT PRIMARY KEY,
    NAME VARCHAR(50)
);

**Update JDBC Credentials in model.java:**

java
Copy
Edit
model m = new model("jdbc:mysql://localhost:3306/student_db", "your_username", "your_password");

---


public class Main {
    public static void main(String[] args) throws Exception {
        model m = new model("jdbc:mysql://localhost:3306/student_db", "root", "password");
        View v = new View();
        controller c = new controller(m, v);
        c.run();
    }
}




javac learn_jdbc/*.java
java learn_jdbc.Main




🤝 Author
Suhail Ahmed
🎓 CS Student | 💡 Aspiring Java Developer | 🧠 Future Data Scientist
🔗 LinkedIn | 🐙 GitHub

📜 License
This project is open-source and available under the MIT License.
