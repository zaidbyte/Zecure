Zecure Security Suite 

Zecure is a sophisticated, modular Windows security application developed in Python. It combines traditional signature-based detection with modern heuristic and structural analysis to provide a multi-layered defense against evolving digital threats.

🛡️ Key Features

Real-Time Protection Shield: An active monitoring system that intercepts file creation and modification events across the filesystem using the watchdog engine.

Multi-Layered Scanning Engine:

Signature Analysis: High-speed SHA-256 hashing matched against a known threat database.

Heuristic Entropy Analysis: Calculates file randomness to detect packed, encrypted, or obfuscated malware payloads (e.g., Ransomware).

PE Header Inspection: Deep analysis of Portable Executable (EXE/DLL) structures to identify suspicious API imports (e.g., CreateRemoteThread) and packing signatures (e.g., UPX).

Modern UI/UX: Built with a high-performance CustomTkinter dashboard featuring dark mode, live activity logs, and asynchronous scan processing.

Asynchronous Execution: Utilizes multi-threading and thread-safe queues to ensure the UI remains responsive during intensive system-wide scans.

Auto-Dependency Management: Self-bootstrapping logic that automatically detects and installs missing Python libraries at runtime.

🚀 Getting Started

Prerequisites

Python 3.9+

Windows OS (Recommended for PE analysis features)

Pip (Python package manager)

Installation

The application is designed to be self-contained. Simply run the main script, and it will handle the installation of required libraries (customtkinter, pefile, psutil, watchdog).

python zecure.py


🛠️ Technical Architecture

1. The Security Engine

The core logic resides in the SecurityEngine class. It assigns a "Suspicion Score" based on:

Entropy Threshold: If a file's entropy exceeds 7.2, it is flagged as a potential high-risk encrypted/packed file.

Import Analysis: Specific Windows APIs used for process injection or hooking increase the threat score.

2. The Real-Time Shield

Utilizes a FileSystemEventHandler that triggers a scan the moment a file is written to the disk. This mimics the behavior of professional "On-Access" scanners.

3. The GUI (ZecureGUI)

Developed using a "Navigation-and-Log" pattern. The UI communicates with the scanning threads via a queue.Queue, preventing the "Application Not Responding" (Freezing) issues common in GUI-based scanners.

⚠️ Disclaimer

Zecure is an educational demonstration of antivirus architecture. While functional, it is intended for research and development purposes and should be used alongside established commercial security solutions.

📜 License

Distributed under the MIT License. See LICENSE for more information.
