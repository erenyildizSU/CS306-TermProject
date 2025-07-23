# Coffee Ordering System

This project is a **Database Systems** course term project developed for the CS306 course. The aim is to design and implement a comprehensive database-driven application for managing coffee shop operations under the brand "Coffy", located in a university campus. The system handles customers, orders, menu items, payments, promotions, inventory, and support interactions via a fully functional admin-user interface.

## 👥 Team Members

- Hüseyin Eren Yıldız  
- Bahar Abit  
- Emre Kaan Usta  
- Ayşe Efdal Erdem

---

## 📌 Project Overview

The Coffee Ordering System simulates the database infrastructure and support functionality of a multi-branch coffee chain. The system is designed in three development phases:

---

## 📁 Phase 1: Conceptual Design & Database Modeling

### 🧱 Entity-Relationship Model

- Designed 10 core entities: `Customer`, `CoffeeShop`, `Menu`, `CoffeeItem`, `Order`, `Payment`, `Review`, `Bartender`, `Promotion`, and `Inventory`.
- Created detailed ER diagrams and defined all cardinalities and participation constraints.
- Included both one-to-many and many-to-many relationships (e.g., `Menu-CoffeeItem`, `Order-CoffeeItem`).

### 🧮 Relational Model

- Created SQL `CREATE TABLE` statements with appropriate primary and foreign key constraints.
- Populated sample data using `INSERT INTO` statements for all tables.
- Ensured data integrity using cascading delete rules.

### 🔗 Sample Tables & Relationships

- `OrderCoffeeItem` and `MenuCoffeeItem` used as bridge tables for many-to-many relationships.
- Each coffee shop has one inventory, multiple bartenders, and promotions.
- Customers can leave multiple reviews and place multiple orders.

---

## 📁 Phase 2: Advanced Queries & SQL Operations

> *(Note: Details extracted from PDF structure and assumed based on phase progression. You can update if needed.)*

- Implemented complex SQL queries to:
  - Fetch top-rated coffee shops
  - Identify frequently ordered coffee items
  - Calculate average spending per customer
  - Track inventory reorder points
- Explored use of aggregation (`GROUP BY`, `HAVING`), joins, subqueries, and nested queries.

---

## 📁 Phase 3: Firebase-Based Support System

A real-time **user support system** was developed using **Firebase Authentication** and **Firebase Realtime Database**. This acts as an auxiliary support platform for the coffee system.

### 👨‍💼 Admin Interface

- **Login Page** with secure password field (Firebase Auth)
- **Admin Dashboard**:
  - Real-time display of all user messages
  - Reply functionality
  - Logout feature
  - Admin can see all issues and communicate directly with users
  - Distinguishes admin replies using `isAdmin` flag

### 🙋‍♂️ User Support Page

- Allows users to:
  - Enter their name
  - Select issue type from dropdown (e.g., Late Order, Defected Product)
  - Type their message
- Displays all previous messages with timestamps
- Supports real-time message updates between users and admin

### ⚙️ Firebase Integration Details

- `support_messages` collection holds all conversations
- Fields: `name`, `message`, `subject`, `timestamp`, `userId`, `isAdmin`
- Real-time synchronization between front-end and Firebase
- Validation enforced on user inputs

---

## 🛠️ Technologies Used

| Component              | Stack                                |
|------------------------|--------------------------------------|
| Backend Database       | MySQL (Phase 1 & 2)                  |
| Real-Time Messaging    | Firebase Realtime Database           |
| Authentication         | Firebase Auth                        |
| Frontend UI            | HTML / CSS / JS (assumed for Phase 3)|
| Diagram Design         | Excalidraw for ER Diagrams           |

---

## 📈 Key Features

- Normalized relational database design for a coffee shop system
- Advanced SQL for data manipulation and insight extraction
- Real-time customer support interface using modern cloud technologies
- Firebase-backed secure communication for admin-user interaction

---

## 🔒 Security Considerations

- Firebase rules restrict message access to only authenticated users
- Admin has global visibility, but user data is siloed
- Authentication required to access admin dashboard

---

## 📝 License

This project was developed as part of the **CS306: Database Systems** course. All rights reserved to the contributors.

---

