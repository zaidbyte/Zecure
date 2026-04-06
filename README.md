# 🛡️ Zecure Security Suite

> A modular, Python-based Windows security application combining signature detection, heuristics, and structural analysis.

---

## 📌 Overview

**Zecure** is a sophisticated, modular security application built in Python. It delivers a **multi-layered defense system** by combining traditional signature-based detection with modern heuristic and structural analysis techniques.

Designed for performance and extensibility, Zecure demonstrates how modern antivirus solutions operate under the hood.

---

## ✨ Features

### 🛡️ Real-Time Protection Shield
- Monitors filesystem activity in real-time  
- Detects file creation and modification instantly  
- Powered by the `watchdog` engine  

### 🔍 Multi-Layered Scanning Engine

#### 🔑 Signature Analysis
- Fast SHA-256 hashing  
- Matches files against a known threat database  

#### 📊 Heuristic Entropy Analysis
- Detects high-entropy files (e.g., packed/encrypted malware)  
- Useful for identifying ransomware and obfuscation  

#### 🧬 PE Header Inspection
- Analyzes EXE/DLL structure  
- Detects:
  - Suspicious API imports (e.g., `CreateRemoteThread`)  
  - Packing signatures (e.g., UPX)  

---

### 🎨 Modern UI/UX
- Built with **CustomTkinter**  
- Dark mode interface  
- Live activity logs  
- Smooth, asynchronous scanning  

---

### ⚡ Asynchronous Execution
- Multi-threaded scanning engine  
- Thread-safe queues  
- Prevents UI freezing during scans  

---

### 🔄 Auto-Dependency Management
- Automatically installs missing libraries at runtime:
  - `customtkinter`
  - `pefile`
  - `psutil`
  - `watchdog`

---

## 🚀 Getting Started

### 📋 Prerequisites
- Python **3.9+**
- Windows OS *(recommended for PE analysis features)*
- `pip` (Python package manager)

---

### 📦 Installation

#### Go to [Releases](https://github.com/zaidbyte/Zecure/releases)
