# AI-Powered Device Login Security System

[cite_start]An intelligent, secure authentication platform built to extend traditional username/password credentials using modern device identification and real-time Artificial Intelligence threat assessment[cite: 52, 310]. [cite_start]This project serves as a highly modular, practical implementation of advanced Object-Oriented Programming (OOP) design patterns and secure engineering guidelines like OWASP[cite: 20, 137].

[cite_start]The system tracks device profiles, maps login behaviors, logs anomalies, and applies machine-learning-driven threat assessments to defend against brute force, unauthorized access, and credential stuffing attacks[cite: 4, 46].

---

## 🚀 Core Features

### 🛡️ Core Security Architecture
* [cite_start]**Cryptographic Password Security:** Enforces strict password policies (minimum 8 characters, uppercase, numbers, and special characters) combined with **SHA-256 hashing and unique random salts**[cite: 60, 94, 374].
* [cite_start]**Proactive Account Lockout:** Mitigates brute-force patterns by dynamically locking out accounts after 3 consecutive failed login attempts[cite: 88, 180].
* [cite_start]**Session Management:** Secure server-side validation models equipped with a 30-minute inactivity expiration window[cite: 162, 390].
* [cite_start]**Device Fingerprinting:** Dynamically extracts and aggregates Browser, OS metadata, User-Agent strings, and platform specifications into a secure identifier string to isolate foreign hardware access[cite: 165, 166, 396].

### 🤖 Artificial Intelligence Integration (OpenAI API)
* [cite_start]**Real-Time Threat Classification:** Sends comprehensive metadata metrics to OpenAI's models (`gpt-4o-mini`) to categorize threats into **LOW, MEDIUM, HIGH, or CRITICAL** parameters[cite: 95, 96].
* [cite_start]**Anomaly Detection:** Tracks access patterns to isolate irregular login times (e.g., midnight to 6 AM) or geographic shifts[cite: 97, 175].
* [cite_start]**Countermeasure Generation:** Generates actionable, context-aware remediation logs and recommendations directly onto the interface dashboards[cite: 98, 99].
* [cite_start]**Resilient Offline Fallback Mode:** Operates natively without an internet connection using deterministic, rule-based algorithmic fallbacks to guarantee uptime[cite: 64, 196].

### Interactive Interface Frameworks
* [cite_start]**Rich GUI Dashboard:** Built with a desktop interface displaying recent login histories, verified trusted devices, live threat indicators, and contextual countermeasures[cite: 119, 183].
* [cite_start]**Console-Based CLI Interface:** A lightweight, colorized console user interface designed for resource-efficient execution[cite: 62, 85].
* [cite_start]**Administrative Controls:** Dedicated administrative screens to inspect system-wide audit records, isolate flagged threats, and release locked student/user accounts[cite: 184].

---

## Technology Stack & Environment

**Language:** Java 17 or higher [cite: 56]
**Paradigm:** Object-Oriented Programming (OOP) [cite: 57]
**AI Integration:** OpenAI API Endpoints [cite: 59]
**Data Storage:** File-based structural logging (`logs/login_attempts.txt` and `intruder_logs/`) [cite: 91, 92]
**User Interfaces:** Java Swing (GUI Windowing) and Console Input Terminal (CLI Mode) [cite: 62, 119]

---

## OOP Principles Implemented

This architecture was designed explicitly around clean coding standards and standard software design abstractions[cite: 20]:

1. **Encapsulation:** Protects internal object fields using private scopes and accessors across all model states (e.g., `User.java`, `LoginAttempt.java`)[cite: 68, 70].
2. **Abstraction:** Employs classes like `AIModel` to encapsulate and shield complex network communications, JSON construction, and HTTP APIs away from consumer layers[cite: 72, 73].
3. **Composition ("has-a" relationship):** Enhances structural maintainability by building major engine states through component assembly—`SecuritySystem` dynamically maps `UserDatabase`, `SecurityLog`, and `AIModel` modules[cite: 75, 76].
4. **Immutability:** Implements data safety by constructing historical logs (like `LoginAttempt`) with strictly final fields, blocking manipulation after recording[cite: 82].
5. **Polymorphism & Constructor Overloading:** Supports flexible instantiations, such as adjusting implicit authorization permissions automatically depending on constructor choices[cite: 78, 79, 80].
6. **Utility Classes:** Leverages static architectures for shared stateless algorithms, including `PasswordHasher` and layout rendering tools like `ConsoleUI`[cite: 83, 84, 85].

---

## Requirement
Ensure you have **Java Development Kit (JDK) 17** or higher installed on your target machine.
