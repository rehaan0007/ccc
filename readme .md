# ⚡ High-Performance Load Balancer in C (Epoll)

## 📖 Description
This project is a TCP Load Balancer written in C using the Linux `epoll` API.  
It efficiently distributes incoming client connections across multiple backend servers using a least-connections algorithm.

---

## 🚀 Key Highlights
- Uses epoll for scalable I/O handling
- Non-blocking sockets
- Full-duplex communication (client ↔ server)
- Greedy load balancing (least connections)
- Handles multiple concurrent connections

---

## 🧠 Load Balancing Strategy
Select the backend server with the minimum active connections.

---

## 🏗️ System Architecture

Load Balancer (Port 9000)
        |
---------------------------------
|        |        |
8001     8002     8003

---

## 📂 Project Structure
load_balancer.c  
README.md  

---

## ⚙️ Prerequisites
- Linux system
- GCC compiler

---

## 🔨 Build
gcc load_balancer.c -o load_balancer

---

## ▶️ Run
./load_balancer

---

## 🖥️ Backend Setup
nc -l 8001  
nc -l 8002  
nc -l 8003  

---

## 🧪 Testing
nc localhost 9000

---

## ⚠️ Limitations
- Blocking connect()
- No health checks
- TCP only

---

## 🔮 Future Enhancements
- Non-blocking connect
- Health monitoring
- Logging
- HTTP support

---

## 👨‍💻 Author
Systems programming project using epoll.
