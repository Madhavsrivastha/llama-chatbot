# 🚀 Llama Chatbot using WasmEdge (Local LLM Deployment)

## 📌 Introduction

This project demonstrates the deployment of a **local Large Language Model (LLM)** using **Llama 3.1** with the **WasmEdge runtime** in a **WSL (Windows Subsystem for Linux)** environment.

Unlike traditional AI systems that depend on cloud infrastructure, this project focuses on running AI models **completely locally**, ensuring **data privacy, cost efficiency, and offline capability**.

The system provides multiple interaction interfaces:

* Command Line Interface (CLI)
* OpenAI-compatible REST API
* Web-based Chatbot UI

Additionally, the application can be exposed publicly using **ngrok**, making it a complete end-to-end deployment solution.

---

## 🎯 Objectives

The main objectives of this project are:

* To understand and implement **local LLM deployment**
* To run **Llama 3.1 GGUF model** using WasmEdge
* To build a **CLI-based chatbot**
* To create an **OpenAI-compatible API server**
* To design a **user-friendly web chatbot interface**
* To expose the local server using **ngrok**

---

## ✨ Key Features

* ✅ Fully local LLM execution (no cloud dependency)
* ✅ CLI-based chatbot interaction
* ✅ REST API compatible with OpenAI format
* ✅ Web-based chatbot interface
* ✅ Public access via ngrok
* ✅ Works on CPU (no GPU required)

---

## 🛠️ Tech Stack

| Component   | Technology            |
| ----------- | --------------------- |
| Runtime     | WasmEdge              |
| Model       | Llama 3.1 (GGUF)      |
| Environment | WSL (Ubuntu)          |
| API         | llama-api-server.wasm |
| CLI         | llama-chat.wasm       |
| UI          | Chatbot UI            |
| Tunneling   | ngrok                 |

---

## 💻 System Requirements

To run this project successfully, the system must meet the following requirements:

* Windows 10 / Windows 11
* WSL2 with Ubuntu installed
* Minimum 8 GB RAM
* Stable Internet connection
* Terminal access
* CPU-based processing (GPU optional)

---

## 🏗️ Project Architecture

```
User Input
   ↓
CLI / Web UI
   ↓
API Server (llama-api-server.wasm)
   ↓
Llama 3.1 Model
   ↓
Response Output
```

This architecture ensures modularity and supports multiple interaction methods.

---

## ⚙️ Setup & Installation Guide

### Step 1: Install WSL & Ubuntu

```bash
wsl --install
```

---

### Step 2: Install WasmEdge

```bash
curl -sSf https://raw.githubusercontent.com/WasmEdge/WasmEdge/master/utils/install.sh | bash
```

---

### Step 3: Download Llama Model

Download the **Llama 3.1 GGUF model** and place it in the project directory.

---

### Step 4: Run CLI Chatbot

```bash
wasmedge run llama-chat.wasm
```

---

### Step 5: Start API Server

```bash
wasmedge run llama-api-server.wasm
```

---

### Step 6: Launch Web UI

Connect the chatbot UI with the API endpoint:

```
http://localhost:8080
```

---

### Step 7: Expose Using ngrok

```bash
ngrok http 8080
```

This generates a public URL to access the chatbot remotely.

---

## 📸 Screenshots

### 🔹 CLI Interaction

![CLI](screenshots/cli.png)

### 🔹 API Response

![API](screenshots/api.png)

### 🔹 Web Chatbot UI

![UI](screenshots/ui.png)

### 🔹 Public Access via ngrok

![ngrok](screenshots/ngrok.png)

---

## 📄 Project Documentation

Detailed documentation is available here:
👉 `docs/project-documentation.pdf`

---

## 📊 Results and Discussion

The project successfully demonstrates the deployment of a local LLM system.

* The CLI interface provides fast and direct interaction
* The API enables seamless integration with external applications
* The Web UI improves usability for non-technical users
* ngrok enables global accessibility

Overall, the system performs efficiently even in CPU-based environments.

---

## ✅ Advantages

* No dependency on cloud services
* Enhanced data privacy
* Cost-effective solution
* Easy to deploy and use
* Multi-interface support

---

## ⚠️ Limitations

* Slower compared to GPU-based systems
* Requires sufficient RAM
* Limited scalability for high workloads

---

## 🔮 Future Scope

* Integration of GPU acceleration
* Improved UI/UX design
* Support for advanced AI features
* Deployment in real-world applications

---

## 🏁 Conclusion

This project presents a complete pipeline for deploying a **local AI chatbot using Llama 3.1 and WasmEdge**.

It highlights how modern AI systems can be built without relying on cloud services, making it a **privacy-focused and cost-efficient solution** for developers and researchers.

---

## 👨‍💻 Author

**Madhav Srivathsa**
B.Tech CSE (Data Science)
Aspiring AI/ML Engineer

---

⭐ If you found this project useful, feel free to star the repository!
