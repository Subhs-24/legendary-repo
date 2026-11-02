# 🛍️ QueueLess — Smart Campus Queue Management System

<p align="center">
  <b>Skip the Queue. Save Your Time. 🚀</b>
</p>

<p align="center">
  A console-based campus queue management system built using C++ and Object-Oriented Programming concepts.
</p>
---

## 📌 Overview

**QueueLess** is a Smart Campus Queue Management System designed to simplify the process of ordering products and services from different campus shops.

Instead of standing in long queues, students can browse available shops, select services, place orders, receive unique token numbers, and track their order status directly through the system.

The system also provides an administrative panel that allows administrators to manage shops, services, and customer orders.

Built entirely in **C++**, this project demonstrates practical implementation of Object-Oriented Programming, file handling, data structures, and basic order management logic.

---

## ✨ Features

### 👨‍🎓 Customer Portal

- 🏪 **Browse Shops** — View all available campus shops.
- 🛒 **Place Orders** — Select a shop, choose a service or product, and specify quantity.
- 🎟️ **Unique Token Generation** — Automatically generates a unique token for every order.
- 💰 **Automatic Bill Calculation** — Calculates the total price based on quantity and service price.
- 📦 **Order Tracking** — Track orders using their token numbers.
- ⏳ **Live Status Updates** — Orders automatically transition from Preparing to Ready based on preparation time when the system checks their status.
- ✅ **Order Collection** — Customers can mark ready orders as collected.

### 🔐 Admin Panel

- 🔑 **Admin Authentication** — Secure access through username and password validation.
- ➕ **Add Shops** — Register new shops in the system.
- ❌ **Remove Shops** — Remove existing shops.
- 🧾 **Add Services** — Add new products or services with their prices.
- 🗑️ **Remove Services** — Remove existing services from shops.
- 📋 **View All Orders** — Monitor customer orders and their current statuses.

### 💾 File Management & Data Persistence

- Automatically saves shop information.
- Stores service details and pricing.
- Maintains customer order records.
- Loads previously saved information when the application starts.
- Uses text files to retain data between program executions.

---

## 🏪 Default Campus Shops

QueueLess comes with four pre-configured shops:

| Shop | Available Products / Services |
|---|---|
| 📚 Stationery | Printout, Practical File, Notebook |
| ☕ Campus Cafe | Coffee, Sandwich, Maggie |
| 🏥 Health Store | Bandage, Face Mask |
| 📄 Photocopy Centre | B&W Copy, Colour Copy |

Administrators can add more shops and services whenever required.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| C++ | Core programming language |
| C++17 | Compilation standard |
| OOP | Class-based program design and inheritance |
| STL Vector | Dynamic storage of shops, services and orders |
| File Handling | Persistent data storage |
| iostream | Console input and output |
| fstream | Reading and writing text files |
| stringstream | Processing stored records |
| ctime | Order timestamps and preparation-time calculations |
| iomanip | Formatted output |

---

## 🧠 OOP Concepts Implemented

This project demonstrates important Object-Oriented Programming concepts:

### 1. Inheritance

QueueLess uses a base class named `User`, from which two derived classes inherit:

- `Customer` — Represents a customer using the system.
- `Admin` — Represents an administrator with authentication functionality.

```cpp
class User {
protected:
    string name;

public:
    User(string n) : name(n) {}

    string getName() const {
        return name;
    }
};

class Customer : public User {
public:
    Customer(string n) : User(n) {}
};

class Admin : public User {
    string password;

public:
    Admin(string n, string p) : User(n), password(p) {}

    bool login(string n, string p) const {
        return name == n && password == p;
    }
};
```

### 2. Encapsulation

The `QueueLess` class encapsulates the system's data and operations, keeping its internal implementation private and exposing the application through its public interface.

### 3. Classes and Objects

The project uses classes such as `User`, `Customer`, `Admin`, and `QueueLess` to organize functionality.

### 4. Data Structures

STL vectors are used to dynamically store:
- Shops
- Services inside each shop
- Customer orders

---

## ⚙️ How It Works

The basic application workflow:

1. The application starts and loads previously saved data.
2. If no shop records exist, default campus shops are created.
3. The user selects either the Customer Portal or Admin Panel.
4. Customers browse shops and place orders.
5. The system generates a unique token and calculates the bill.
6. Order information is saved to text files.
7. The system checks elapsed preparation time and updates order status.
8. Customers track and collect their orders.
9. Administrators manage shops, services, and orders.

---

## 📂 Project Structure

```text
QueueLess/
│
├── QueueLess_Approx400.cpp   # Main C++ source code
│
├── shops.txt                 # Stores shop records
├── services.txt              # Stores service records
├── orders.txt                # Stores customer orders
│
└── README.md                 # Project documentation
```

**Note:** The `.txt` files are generated automatically when the application creates or saves data. They do not need to be manually created beforehand.

---

## 🚀 Getting Started

### Prerequisites

- A C++ compiler supporting C++17.
- Visual Studio Code, Code::Blocks, or any compatible C++ IDE.
- GCC / MinGW (if compiling through the terminal).

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/QueueLess.git
```

### 2. Navigate to the Project Directory

```bash
cd QueueLess
```

### 3. Compile the Source Code

```bash
g++ -std=c++17 QueueLess_Approx400.cpp -o QueueLess
```

### 4. Run the Application

**Windows:**

```bash
QueueLess.exe
```

**Linux / macOS:**

```bash
./QueueLess
```

---

## 🔑 Admin Login Credentials

Use the following default credentials to access the Admin Panel:

| Field | Credentials |
|---|---|
| Username | `admin` |
| Password | `admin123` |

> ⚠️ These are demonstration credentials hardcoded in the source code. They should be changed before any real-world deployment.

---

## 🔮 Future Improvements

Some features that could make QueueLess even more powerful:

- 🌐 Web-based interface for students and administrators.
- 🗄️ MySQL database integration.
- 📱 Mobile application support.
- 🔔 Real-time order notifications.
- 📊 Sales and order analytics dashboard.
- 👤 Individual customer accounts and order history.
- 🔒 Improved authentication and password security.
- 🏬 Support for multiple campus locations.

---

## 🎯 Learning Outcomes

Through this project, the following concepts were explored:

- Practical implementation of Object-Oriented Programming in C++.
- Understanding inheritance through base and derived classes.
- Working with STL vectors and structured data.
- Implementing file handling for persistent storage.
- Designing a menu-driven application.
- Managing orders, unique tokens, and status transitions.
- Organizing a real-world problem into a working software solution.

---

## 👨‍💻 Project Information

| Detail | Information |
|---|---|
| Project Name | QueueLess |
| Project Type | Smart Campus Queue Management System |
| Language | C++ |
| Standard | C++17 |
| Application Type | Console-Based |
| Storage | Local Text Files |
| Focus | Object-Oriented Programming |

---

<p align="center">
  <b>Built using C++</b>
  <br>
  <i>QueueLess — Making campus queues a little less crowded.</i> 🚀
</p>
