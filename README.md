
---
 
### **📌 `README.md` for Inventory Management System**

# 🏪 Inventory Management System 
 
This is a **CRUD application for an Inventory Management System**  built with **Golang (Gin framework)** and **JWT-based authentication**.  
It provides basic **CRUD operations** for managing inventory items with user authentication.
 
---
 
## 🚀 **Getting Started**
Follow these steps to **clone the repository, set up dependencies, configure JWT authentication, and start using the application.**
 
### **1️⃣ Clone the Repository**
Ensure **Git** is installed, then run:
 
```sh
git clone https://github.com/AryanNema7/inventory_management.git
cd inventory_management
```
 
---
 
## 🛠️ **Prerequisites**
### **2️⃣ Install Go (if not installed)**
Make sure **Go 1.20+** is installed.
 
#### **🔹 Windows**
Download and install Go from:  
🔗 [Go Official Website](https://go.dev/dl/)  
Verify installation:
```powershell
go version
```
 
#### **🔹 Linux (Debian/Ubuntu)**
```sh
sudo apt update && sudo apt install -y golang
go version
```
 
#### **🔹 macOS (Homebrew)**
```sh
brew install go
go version
```
 
---
 
## 🔧 ** Install Project Dependencies**
Once Go is installed, run:
```sh
cd < `project-folder-where-you-cloned-the-repo` >
go mod tidy
```
This will download all required dependencies.
 
---

---
📦  **Install Required Go Modules**
Before running the application, install all dependencies using:

```sh

go mod tidy
```
This will download the necessary modules for the project.

✅ Ensure the following required modules are installed (if there is any error in `go mod tidy` manually install following):

```sh

go get github.com/gin-gonic/gin
go get github.com/golang-jwt/jwt/v5
go get github.com/glebarez/sqlite
go get github.com/joho/godotenv
go get github.com/gin-contrib/cors
go get github.com/ulule/limiter/v3
If any module is missing, manually install it using:
```
If any module is missing, manually install it using:
```sh

go get <module_name>
```
---
 
## 🔑 **4️⃣ Set Up JWT Authentication**
This application requires a **JWT_SECRET_KEY** for authentication.
 
### **🔹 Generate a Secure JWT Secret Key**
Use **OpenSSL** to generate a secure secret key.
 
#### **Windows (PowerShell)**
```powershell
"JWT_SECRET_KEY=$(openssl rand -base64 32)" | Out-File -Encoding ascii .env
```
 
#### **Linux/macOS**
```sh
echo "JWT_SECRET_KEY=$(openssl rand -base64 32)" > .env
```
 
To persist this value across sessions, **add it to `~/.bashrc` or `~/.zshrc`**.
 
---
 
## 🔑 **5️⃣ Install OpenSSL (If Not Installed)**
OpenSSL is required for generating secure JWT keys.
 
### **🔹 Windows**
If `openssl` is not recognized, install it via **Chocolatey**:
```powershell
choco install openssl
```
Verify installation:
```powershell
openssl version
```
 
### **🔹 Linux (Debian/Ubuntu)**
```sh
sudo apt install -y openssl
openssl version
```
 
### **🔹 macOS (Homebrew)**
```sh
brew install openssl
openssl version
```
 
---
 
## ▶️ **6️⃣ Run the Application**
After setup, start the application using:
```sh
go run main.go
```
Once started, the server will be running on **`http://localhost:8080`**.
 
### **Login & Signup API Endpoints**
| **Method** | **Endpoint**         | **Description**               |
|-----------|----------------------|------------------------------|
| `POST`    | `/signup`            | Register a new user          |
| `POST`    | `/login`             | Authenticate and get JWT     |
| `GET`     | `/items`             | Fetch inventory items        |
| `POST`    | `/items`             | Add new inventory item       |
| `DELETE`  | `/items/:id`         | Delete inventory item        |
 
---
 
## 🎯 **Next Steps**
- Access the **inventory management UI** at: `http://localhost:8080`
- Login or Sign up and start managing your inventory.
 
---
 
## ❓ **Troubleshooting**
**c
 
**🔹 Facing Permission Issues on Windows?**  
Run PowerShell as Administrator and try:
```powershell
Set-ExecutionPolicy Unrestricted -Scope CurrentUser
```
 
**🔹 `.env` Not Loading?**  
Delete and recreate it:
```sh
echo "JWT_SECRET_KEY=$(openssl rand -base64 32)" > .env
```
 
---
 
## 📜 **License**
This is a **PoC project** and is provided **without warranties**.
 
---
 
🚀 **Now you're ready to use the Inventory Management System!** 🚀
```
 
---
 
## **📌 What This README Covers**
✅ **How to clone the repo**  
✅ **How to install Go**  
✅ **How to install dependencies (`go mod tidy`)**  
✅ **How to set up JWT authentication using OpenSSL**  
✅ **How to install OpenSSL on Windows/Linux/macOS**  
✅ **How to start the application (`go run main.go`)**  
✅ **How to interact with APIs**  
✅ **Troubleshooting common issues**  
 
---