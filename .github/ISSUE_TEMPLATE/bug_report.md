---
name: Bug Report
about: Report a reproducible bug in the StreamAudio YouTube Downloader Web App
title: "[BUG] - Summary of the bug"
labels: bug
assignees: "chirag127"

--- 

### Describe the bug

A clear and concise description of what the bug is. What happened and what was the expected behavior?

### To Reproduce

Steps to reproduce the behavior:
1. Go to '...' website
2. Click on '....' button
3. Scroll down to '....'
4. See error

### Expected Behavior

Explain what you expected to happen.

### Screenshots

If applicable, add screenshots to help explain your problem. You can drag files here to upload them.

### Environment

*   **App Version:** (e.g., 1.0.0)
*   **Python Version:** (e.g., 3.10.x)
*   **Streamlit Version:** (e.g., 1.x.x)
*   **yt-dlp Version:** (e.g., 2023.x.x)
*   **Operating System:** (e.g., Windows 10, macOS Ventura, Ubuntu 22.04)
*   **Browser (if applicable):** (e.g., Chrome 115, Firefox 110)

### Additional Context

Add any other context about the problem here. For example, specific YouTube URLs that cause issues, unusual network conditions, etc.

### AI Agent Directives Adherence

*   **System Architecture:** Modular Monolith principles are expected to be maintained. This bug report pertains to the Python-based Streamlit application.
*   **Verification Commands:** Please ensure testing and debugging efforts align with Apex standards. Relevant commands for this stack include:
    *   `uv run src/app.py` (To run the application)
    *   `ruff check .` (For linting)
    *   `pytest` (For running tests)
*   **Reporting:** This report follows the established Apex bug reporting template, ensuring clarity and reproducibility for development teams.
