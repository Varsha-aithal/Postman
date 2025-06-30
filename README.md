# 🧪 Booker API – Postman Automation Project

This project contains automated API tests for the [Restful Booker API](https://restful-booker.herokuapp.com/apidoc/index.html), using **Postman** for request scripting and **Newman** for CLI-based execution.

---

## 📌 Scope

The purpose of this project is to test all major endpoints of the Booker API through automated test scripts written in **Postman**. Each request has associated tests verifying functionality, status codes, and response data.

---

## 🌐 Website Tested

**API Documentation:**  
🔗 [https://restful-booker.herokuapp.com/apidoc/index.html](https://restful-booker.herokuapp.com/apidoc/index.html)

---

## 📂 Covered API Requests

### 🔹 Ping – Health Check
- **Endpoint:** `GET /ping`
- **Purpose:** Checks if the API is up and running.

### 🔹 Auth – Create Token
- **Endpoint:** `POST /auth`
- **Purpose:** Creates a new authentication token to use for accessing protected endpoints like `PUT` and `DELETE /booking`.

### 🔹 Booking – Get Booking IDs
- **Endpoint:** `GET /booking`
- **Purpose:** Returns the IDs of all bookings currently present in the API.

### 🔹 Booking – Get Booking by ID
- **Endpoint:** `GET /booking/{id}`
- **Purpose:** Retrieves a specific booking using a valid booking ID.

### 🔹 Booking – Create Booking
- **Endpoint:** `POST /booking`
- **Purpose:** Creates a new booking with user-provided details like name, dates, and deposit status.

### 🔹 Booking – Update Booking
- **Endpoint:** `PUT /booking/{id}`
- **Purpose:** Fully updates an existing booking. Requires token-based authorization.

### 🔹 Booking – Partial Update Booking
- **Endpoint:** `PATCH /booking/{id}`
- **Purpose:** Partially updates an existing booking with selected fields.

### 🔹 Booking – Delete Booking
- **Endpoint:** `DELETE /booking/{id}`
- **Purpose:** Deletes an existing booking. Requires token-based authorization.

---

## 🔧 Tools & Technologies

- **Postman** – For designing and scripting API requests.
- **Newman** – CLI tool for running Postman collections.
- **JavaScript (PM scripting)** – For validations, dynamic variables, and chaining.
- **Postman Environment Variables** – To manage token, booking IDs, and reuse across requests.

---

## ▶️ How to Run

1. Clone the repository.
2. Import the Postman collection and environment into your Postman app.
3. Run the collection using Postman or through the command line with Newman.

```bash
newman run Booker_API_Collection.json -e Booker_API_Environment.json
