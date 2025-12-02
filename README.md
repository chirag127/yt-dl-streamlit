# StreamAudio-YouTube-Downloader-Web-App

![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/StreamAudio-YouTube-Downloader-Web-App/ci.yml?style=flat-square&label=Build)
[![Coverage](https://codecov.io/gh/chirag127/StreamAudio-YouTube-Downloader-Web-App/branch/main/graph/badge.svg?style=flat-square)](https://codecov.io/gh/chirag127/StreamAudio-YouTube-Downloader-Web-App)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/StreamAudio-YouTube-Downloader-Web-App?style=flat-square)](https://github.com/chirag127/StreamAudio-YouTube-Downloader-Web-App)
[![License](https://img.shields.io/github/license/chirag127/StreamAudio-YouTube-Downloader-Web-App?style=flat-square)](LICENSE)
![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square)
![Framework](https://img.shields.io/badge/Framework-Streamlit-47d494?style=flat-square)
[![Ruff Status](https://img.shields.io/badge/Linter-Ruff-8a418b?style=flat-square)](https://github.com/charliermarsh/ruff)


## ⭐️ Star this Repo

[<img src="https://img.shields.io/badge/Star%20%E2%98%85%EF%B8%8F%20this%20Repo-blue?style=flat-square&logo=github" alt="Star this Repo">](https://github.com/chirag127/StreamAudio-YouTube-Downloader-Web-App)

StreamAudio is a high-performance, Streamlit-based web interface providing robust **YouTube audio extraction** capabilities, underpinned by the battle-tested `yt-dlp` library. This project enforces modern Python development standards for maintainability and future-proofing.

This repository serves as a professional reference implementation for building production-ready data extraction utilities using Python's scientific and web ecosystem.

---

### 🌳 Architecture Overview

The architecture follows a clear separation of concerns, typical of a **Modular Monolith**, ensuring the UI layer (Streamlit) remains decoupled from the core business logic (yt-dlp interfacing and data processing).

mermaid
flowchart TD
    A[User Interface: Streamlit Web App] -->|HTTP Request| B(Application Controller/Service Layer)
    B --> C{Core Business Logic: Audio Extraction}
    C -->|Invokes| D[External Adapter: yt-dlp CLI/Library]
    D -->|Downloads/Processes| E[(YouTube Source Data)]
    C --> F(Error Handling & Logging)
    B --> G[Configuration & State Management]
    F --> H[System Logs]


### 📜 Table of Contents

1.  [Features](#-features)
2.  [Technology Stack](#-technology-stack)
3.  [Installation & Setup](#-installation--setup)
4.  [Usage](#-usage)
5.  [Development & Testing](#-development--testing)
6.  [Contributing](#-contributing)
7.  [License](#-license)
8.  [🤖 AI Agent Directives](#-ai-agent-directives)

---

## ✨ Features

*   **Robust Extraction:** Utilizes `yt-dlp` for reliable handling of various YouTube stream formats and metadata.
*   **Streamlit Interface:** Provides a user-friendly, responsive web application for easy interaction.
*   **Modern Python Practices:** Enforces strict type hinting, configuration management, and dependency resolution via `uv`.
*   **Automated Quality Checks:** CI/CD pipeline ensures code quality, coverage, and build integrity on every push.
*   **Audio Format Selection:** Ability to specify desired output formats (e.g., MP3, M4A).

## 🛠 Technology Stack

| Component | Technology | Standard/Version |
| :--- | :--- | :--- |
| **Primary Language** | Python | 3.10+ |
| **Web Framework** | Streamlit | Latest Stable |
| **Core Utility** | `yt-dlp` | Latest |
| **Package Manager** | `uv` | Latest |
| **Linting/Formatting**| `Ruff` | Latest |
| **Testing** | `Pytest` | Latest |
| **CI/CD** | GitHub Actions | Standard Workflow |

## 🚀 Installation & Setup

Follow these steps to set up the development environment. This project is managed using the **Apex Python Toolchain**.

bash
# 1. Clone the repository
git clone https://github.com/chirag127/StreamAudio-YouTube-Downloader-Web-App.git
cd StreamAudio-YouTube-Downloader-Web-App

# 2. Create and activate a virtual environment using uv
uv venv
source .venv/bin/activate  # On Linux/macOS
# .venv\Scripts\activate    # On Windows

# 3. Install dependencies
uv install -e .[dev]

# 4. Run initial checks (Linting/Formatting enforced by Ruff)
ruff check .


## ▶️ Usage

To launch the Streamlit application locally:

bash
streamlit run app.py


*(Note: Replace `app.py` with the actual main entry point file name if different.)*

## 🧪 Development & Testing

We adhere strictly to the DRY and SOLID principles. All core logic is unit-tested with Pytest.

| Command | Description |
| :--- | :--- |
| `uv run pytest` | Execute all unit and integration tests. |
| `uv run pytest --cov` | Execute tests with coverage reporting. |
| `ruff format .` | Enforce code formatting style. |
| `ruff check .` | Run static analysis and linting checks. |

## 🤝 Contributing

Please refer to the detailed guidelines in `.github/CONTRIBUTING.md`.

## 📄 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International License**. See the [LICENSE](LICENSE) file for details.

---

<details>
<summary>🤖 AI Agent Directives (System Configuration)</summary>

# SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs. Verify external dependencies.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends** related to media extraction.
    *   **Validation:** Use `docfork` to verify *every* external API signature (e.g., `yt-dlp` interface).
    *   **Reasoning:** Engage `clear-thought-two` to architect robust extraction pipelines *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** Detect the project type (`pyproject.toml` for Python) and apply the corresponding **Apex Toolchain**.

*   **PRIMARY SCENARIO: DATA / SCRIPTS / AI (Python)**
    *   **Stack:** This project leverages **Python 3.10+**. Key tools include **uv** (for package management and dependency resolution), **Ruff** (for ultra-fast linting and formatting), and **Pytest** (for robust unit and integration testing).
    *   **Architecture:** Adheres to a **Modular Monolith** pattern, ensuring clear separation of concerns for UI, service layer, and the `yt-dlp` adapter. Prioritize robust I/O handling.
    *   **Security:** Critical focus on sanitizing all user-provided input before passing it to external system calls (`yt-dlp`).

## 4. ARCHITECTURAL PRINCIPLES (MANDATORY ADHERENCE)
*   **SOLID:** Applied rigorously, especially Single Responsibility Principle (SRP) to isolate UI logic from extraction logic.
*   **DRY:** Avoid duplication, especially in configuration loading.
*   **YAGNI:** Only build functionality explicitly required by the core mission (YouTube Audio Extraction).

## 5. VERIFICATION COMMANDS (ENTRY POINTS)
*   **Lint & Format:** `ruff check .` and `ruff format .`
*   **Test Suite:** `uv run pytest --cov=./ --cov-report=term-missing --cov-report=xml:coverage.xml`
*   **Build/Run:** `streamlit run <main_file>.py`
*   **Environment Setup:** `uv sync`

</details>
