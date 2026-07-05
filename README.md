# AI-Powered Device Login Security System

An intelligent, secure authentication platform built to extend traditional username/password credentials using modern device identification and real-time Artificial Intelligence threat assessment. This project serves as a highly modular, practical implementation of advanced Object-Oriented Programming (OOP) design patterns and secure engineering guidelines like OWAS.

The system tracks device profiles, maps login behaviors, logs anomalies, and applies machine-learning-driven threat assessments to defend against brute force, unauthorized access, and credential stuffing attacks.

---

## Core Features

### Core Security Architecture
**Cryptographic Password Security:** Enforces strict password policies (minimum 8 characters, uppercase, numbers, and special characters) combined with **SHA-256 hashing and unique random salts**.
**Proactive Account Lockout:** Mitigates brute-force patterns by dynamically locking out accounts after 3 consecutive failed login attempts.
**Session Management:** Secure server-side validation models equipped with a 30-minute inactivity expiration window.
**Device Fingerprinting:** Dynamically extracts and aggregates Browser, OS metadata, User-Agent strings, and platform specifications into a secure identifier string to isolate foreign hardware acces.

### Artificial Intelligence Integration (OpenAI API)
**Real-Time Threat Classification:** Sends comprehensive metadata metrics to OpenAI's models (`gpt-4o-mini`) to categorize threats into **LOW, MEDIUM, HIGH, or CRITICAL** parameters.
**Anomaly Detection:** Tracks access patterns to isolate irregular login times (e.g., midnight to 6 AM) or geographic shifts.
**Countermeasure Generation:** Generates actionable, context-aware remediation logs and recommendations directly onto the interface dashboards.
**Resilient Offline Fallback Mode:** Operates natively without an internet connection using deterministic, rule-based algorithmic fallbacks to guarantee uptime.

### Interactive Interface Frameworks
**Rich GUI Dashboard:** Built with a desktop interface displaying recent login histories, verified trusted devices, live threat indicators, and contextual countermeasures.
**Console-Based CLI Interface:** A lightweight, colorized console user interface designed for resource-efficient execution.
**Administrative Controls:** Dedicated administrative screens to inspect system-wide audit records, isolate flagged threats, and release locked student/user accounts.

---

## Technology Stack & Environment

**Language:** Java 17 or higher 
**Paradigm:** Object-Oriented Programming (OOP)
**AI Integration:** OpenAI API Endpoints
**Data Storage:** File-based structural logging (`logs/login_attempts.txt` and `intruder_logs/`)
**User Interfaces:** Java Swing (GUI Windowing) and Console Input Terminal (CLI Mode) 

---

## OOP Principles Implemented

This architecture was designed explicitly around clean coding standards and standard software design abstractions:

1. **Encapsulation:** Protects internal object fields using private scopes and accessors across all model states (e.g., `User.java`, `LoginAttempt.java`).
2. **Abstraction:** Employs classes like `AIModel` to encapsulate and shield complex network communications, JSON construction, and HTTP APIs away from consumer layers.
3. **Composition ("has-a" relationship):** Enhances structural maintainability by building major engine states through component assembly—`SecuritySystem` dynamically maps `UserDatabase`, `SecurityLog`, and `AIModel` modules.
4. **Immutability:** Implements data safety by constructing historical logs (like `LoginAttempt`) with strictly final fields, blocking manipulation after recording.
5. **Polymorphism & Constructor Overloading:** Supports flexible instantiations, such as adjusting implicit authorization permissions automatically depending on constructor choices.
6. **Utility Classes:** Leverages static architectures for shared stateless algorithms, including `PasswordHasher` and layout rendering tools like `ConsoleUI`.

---

## Requirement
Ensure you have **Java Development Kit (JDK) 17** or higher installed on your target machine.
