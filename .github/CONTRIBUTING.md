# 🤝 Contributing to StreamAudio-YouTube-Downloader-Web-App

We welcome contributions that uphold the Apex Technical Authority standards of Zero-Defect, High-Velocity, and Future-Proof engineering. This project, focused on robust audio extraction using Python and `yt-dlp`, requires adherence to specific guidelines.

## 1. Core Principles (The Apex Mandate)

Before contributing, please internalize the core architectural philosophy:

*   **SOLID Compliance:** Every new module or class must demonstrate clear adherence to SOLID principles.
*   **DRY Enforcement:** Avoid all code duplication. Leverage existing abstractions.
*   **YAGNI & FUTURE-PROOFING:** Implement only what is currently required, but design interfaces and dependency injections that allow for seamless future upgrades (e.g., swapping `yt-dlp` for a hypothetical `yt-dlp-v2` without refactoring core business logic).
*   **Toolchain Alignment:** Use `uv` for dependency management, `Ruff` for linting/formatting, and `Pytest` for testing.

## 2. Contribution Workflow

All contributions must follow this strict lifecycle:

1.  **Fork & Clone:** Fork the repository and clone your fork locally.
    bash
    git clone https://github.com/YOUR_USERNAME/StreamAudio-YouTube-Downloader-Web-App.git
    cd StreamAudio-YouTube-Downloader-Web-App
    
2.  **Branching Strategy:** Create a feature branch off `main` using the conventional prefix:
    *   `feat/`: For new features.
    *   `fix/`: For bug fixes.
    *   `refactor/`: For non-functional improvements.
    *   `docs/`: For documentation changes.
    
    Example: `git checkout -b feat/add-progress-bar`
3.  **Development & Verification:** Implement your changes. **Crucially, new features MUST include comprehensive unit tests covering 90%+ of new logic paths using `Pytest` to maintain coverage standards.**
4.  **Linting & Formatting:** Ensure your code is pristine before committing.
    bash
    # Run formatter and linter via Ruff (ensuring alignment with Apex standards)
    uv run ruff check --fix .
    uv run ruff format .
    
5.  **Commit Messages:** Use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).
    *   *Good:* `feat(extractor): Introduce async handling for yt-dlp calls`
    *   *Bad:* `fixed stuff`
6.  **Pull Request (PR):** Push your branch to your fork and open a Pull Request against `chirag127/main`.
    *   **Use the official PR Template** (`.github/PULL_REQUEST_TEMPLATE.md`).
    *   Reference any related issues using `Closes #ISSUE_NUMBER`.

## 3. Bug Reporting

If you discover an issue, please use the official **Bug Report Template** located in `.github/ISSUE_TEMPLATE/bug_report.md`. Provide detailed reproduction steps, environment details (OS, Python version), and expected vs. actual behavior.

## 4. Code Style & Standards

### Python Dependencies
All dependencies must be managed via `pyproject.toml` using the `uv` toolchain. We favor static typing (`mypy` checks enforced via Ruff).

### Streamlit UI
When updating the UI components, prioritize performance and accessibility. Adhere to the principle of minimal re-renders. Avoid embedding complex logic directly into Streamlit callbacks; delegate to separate, testable Python modules.

## 5. Security Guidelines

For security-sensitive contributions, please review the repository's security policy in `.github/SECURITY.md` and use appropriate channels for responsible disclosure if necessary. **Never hardcode sensitive tokens or keys.** Use environment variables exclusively.

Thank you for helping elevate `StreamAudio-YouTube-Downloader-Web-App` to the 2026 standard!