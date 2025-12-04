# StreamAudio-YouTube-Audio-Extractor-Web-App

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/chirag127/StreamAudio-YouTube-Audio-Extractor-Web-App/ci.yml?label=Build&style=flat-square)
![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/StreamAudio-YouTube-Audio-Extractor-Web-App?style=flat-square)
![Python Version](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square)
![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blueviolet?style=flat-square)
![GitHub Stars](https://img.shields.io/github/stars/chirag127/StreamAudio-YouTube-Audio-Extractor-Web-App?style=flat-square)

[![Star this Repo](https://img.shields.io/github/stars/chirag127/StreamAudio-YouTube-Audio-Extractor-Web-App?style=social&color=yellow)](https://github.com/chirag127/StreamAudio-YouTube-Audio-Extractor-Web-App/stargazers)

StreamAudio is a robust, high-performance Streamlit web application designed for the deterministic extraction and conversion of audio tracks from YouTube URLs. Utilizing the powerful `yt-dlp` engine under a modern Python modular architecture, this solution offers reliability and maintainability for high-volume media processing tasks.

## 🏗️ Architecture Overview

This project adheres to the principles of a **Modular Monolith**, ensuring clear separation between the Presentation Layer (Streamlit UI), Service Layer (Core Logic/yt-dlp wrappers), and Utility Layer (Configuration/Logging). Error handling is deterministic, following the **Apex Zero-Defect Mandate**.

text
StreamAudio-YouTube-Audio-Extractor-Web-App/
├── src/
│   ├── core/                 # Business logic, yt-dlp wrappers
│   ├── services/
│   │   └── extractor.py      # Primary audio extraction service
│   ├── ui/
│   │   └── app.py            # Streamlit Presentation Layer
│   └── utils/
│       └── config.py         # Configuration management
├── tests/
│   ├── unit/
│   └── integration/
├── .venv/
├── pyproject.toml            # Dependency management (uv)
└── README.md


## 📑 Table of Contents

1.  [🚀 Key Features](#-key-features)
2.  [🛠️ Tech Stack (Apex Standard)](#-tech-stack-apex-standard)
3.  [🤖 AI Agent Directives](#-ai-agent-directives)
4.  [⚙️ Setup & Development](#-setup--development)
5.  [💡 Development Principles](#-development-principles)
6.  [📜 License](#-license)

## 🚀 Key Features

*   **Robust Extraction:** Leverages `yt-dlp` for best-in-class format detection and downloading.
*   **Streamlit Interface:** Provides an intuitive, responsive web GUI for non-CLI users.
*   **Format Control:** Allows specification of desired output audio formats (MP3, M4A, WAV).
*   **Modular Design:** Clear separation of concerns adhering to modern Python best practices.
*   **CI/CD Ready:** Full GitHub Actions pipeline for automated testing and linting.

## 🛠️ Tech Stack (Apex Standard)

| Category | Technology | Version Constraint |
| :--- | :--- | :--- |
| Language | Python | 3.10+ |
| Dependency Management | uv | Latest Stable |
| Linting/Formatting | Ruff | Strict Enforcement |
| Testing Framework | Pytest | Comprehensive Coverage |
| Web Framework | Streamlit | Current Stable |
| Media Engine | yt-dlp | Latest Stable |

## 🤖 AI Agent Directives

<details>
<summary>Click to view Apex Execution Directives for this Repository</summary>

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
    *   **No Guessing:** Do not hallucinate APIs. You must use the installed library features (`yt-dlp` CLI wrapper logic).
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards** related to video/audio extraction compliance and security.
    *   **Validation:** Use `docfork` to verify *every* external command signature (e.g., `yt-dlp --extract-audio`).
    *   **Reasoning:** Engage `clear-thought-two` to architect complex media processing flows *before* writing code, prioritizing thread safety if applicable.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** This repository is a Python-based Media Processing Tool.

*   **PRIMARY SCENARIO: DATA / SCRIPTS / AI (Python)**
    *   **Stack:** This project leverages **Python 3.10+**. Key tools include **uv** (for package management and dependency resolution), **Ruff** (for ultra-fast linting and formatting), and **Pytest** (for robust unit and integration testing).
    *   **Architecture:** Adheres to a **Modular Monolith** pattern, ensuring clear separation of concerns for the Streamlit interface and the `yt-dlp` service layer. Prioritize clean API contracts between UI components and the extraction engine.
    *   **Dependency Focus:** Ensure all interaction with external binaries (`yt-dlp`) is encapsulated and idempotent where possible.

---

## 4. VERIFICATION & EXECUTION COMMANDS

| Command Type | Description | Command |
| :--- | :--- | :--- |
| Dependency Setup | Initialize environment and install dependencies | `uv sync` |
| Formatting/Linting | Run Ruff formatter and linter | `ruff check . && ruff format .` |
| Unit Testing | Execute all unit tests | `pytest tests/unit` |
| Full CI Simulation | Run local equivalent of the CI pipeline | `uv run build_and_test` (See scripts below) |

**Apex Verification Strategy:** All code changes **MUST** pass Ruff linting and achieve >90% test coverage on modified logic blocks. Extraction wrappers must handle `KeyError` and connection timeouts gracefully.

</details>

## ⚙️ Setup & Development

This repository mandates the use of `uv` for deterministic dependency management.

### Prerequisites

1.  Python 3.10 or newer installed.
2.  `yt-dlp` binary installed globally, or configured to be downloaded by the script (Preferred: Ensure installation via `uv sync` if packaged as a dependency).

### Installation

bash
# 1. Clone the repository
git clone https://github.com/chirag127/StreamAudio-YouTube-Audio-Extractor-Web-App.git
cd StreamAudio-YouTube-Audio-Extractor-Web-App

# 2. Create and activate virtual environment (uv handles this implicitly, but good practice)
# uv venv

# 3. Install dependencies using uv
# Assumes pyproject.toml defines dependencies correctly
uv sync


### Execution Scripts

| Script Name | Command | Purpose |
| :--- | :--- | :--- |
| `start-web` | `uv run start-web` | Launches the Streamlit application |
| `test-all` | `uv run test-all` | Runs linting, formatting, and all Pytest suites |
| `check-deps` | `uv check` | Verifies the dependency graph |

## 💡 Development Principles

All development within this repository must strictly adhere to the following architectural tenets:

1.  **SOLID:** Especially Single Responsibility (ensuring extraction logic is separate from UI rendering).
2.  **DRY:** Avoid duplication, particularly in configuration loading or error message generation.
3.  **YAGNI:** Implement only the functionality required for robust audio extraction; avoid speculative complexity.
4.  **Future-Proofing:** Use Python 3.10+ features where they improve clarity and performance (e.g., structural pattern matching, if applicable to logic flow).

## 📜 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International License**. See the [LICENSE](./LICENSE) file for details.
