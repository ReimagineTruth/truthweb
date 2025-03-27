# Contributing to TruthWeb Project

Welcome to the TruthWeb Project! We're building a decentralized platform powered by the Pi Network, and we’re thrilled to have you consider contributing. Whether you're a developer, designer, tester, or documentation enthusiast, your contributions help us create a robust, community-driven web experience for Pi Network users. This guide outlines how you can get involved.

## Table of Contents
1. [Code of Conduct](#code-of-conduct)
2. [About TruthWeb](#about-truthweb)
3. [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Setup](#setup)
4. [How to Contribute](#how-to-contribute)
   - [Reporting Bugs](#reporting-bugs)
   - [Suggesting Features](#suggesting-features)
   - [Submitting Pull Requests](#submitting-pull-requests)
5. [Development Guidelines](#development-guidelines)
   - [Coding Standards](#coding-standards)
   - [Testing](#testing)
6. [Community](#community)
7. [Contact](#contact)

---

## Code of Conduct
We’re committed to fostering an inclusive and respectful community. By contributing, you agree to uphold our [Code of Conduct](CODE_OF_CONDUCT.md) (to be created if not present). Please treat everyone with kindness and respect.

---

## About TruthWeb
TruthWeb is a decentralized web platform designed for the Pi Network community. It leverages the Pi SDK for secure authentication and payments, aiming to provide a seamless, user-friendly experience for Pioneers. This repository focuses on the Pi Authentication component, a key feature enabling users to log in using their Pi Network credentials.

---

## Getting Started

### Prerequisites
- **Node.js**: Version 16+ ([Download](https://nodejs.org/)).
- **Git**: For version control ([Download](https://git-scm.com/)).
- **Pi Browser**: Required for testing Pi SDK features (available on iOS/Android).
- **Text Editor**: We recommend VS Code for its JavaScript and HTML support.

### Setup
1. **Fork and Clone the Repository**:
   - Fork the TruthWeb repository on GitHub: `https://github.com/truthweb/pi-auth-project` (replace with actual URL).
   - Clone your fork:
     ```bash
     git clone https://github.com/your-username/pi-auth-project.git
     cd pi-auth-project
     ```

2. **Backend Setup**:
   - Navigate to the backend:
     ```bash
     cd backend
     ```
   - Install dependencies:
     ```bash
     npm install
     ```
   - Create a `.env` file:
     ```plaintext
     PORT=3000
     PI_API_KEY=your_pi_network_api_key_here  # Optional for sandbox mode
     ```
   - Start the server:
     ```bash
     npm start
     ```

3. **Frontend Setup**:
   - Navigate to the frontend:
     ```bash
     cd ../frontend
     ```
   - Install live-server (optional):
     ```bash
     npm install
     ```
   - Serve the frontend:
     ```bash
     npm start
     ```
   - Open `http://localhost:8080/auth.html` in the Pi Browser (sandbox mode).

---

## How to Contribute

### Reporting Bugs
- Check the [Issues](https://github.com/truthweb/pi-auth-project/issues) tab for existing bug reports.
- If your bug isn’t listed, open a new issue with:
  - Title: e.g., "Authentication fails with invalid token"
  - Description: Steps to reproduce, expected vs. actual behavior, and screenshots/logs if possible.
  - Label it as "bug."

### Suggesting Features
- Open an issue labeled "enhancement" or "feature request."
- Example: "Add logout confirmation dialog."
- Include:
  - Why the feature matters to TruthWeb users.
  - A rough idea of how it could work (optional).
- Discuss with the team before coding to ensure it fits the project vision.

### Submitting Pull Requests
1. **Create a Branch**:
   - Name it descriptively (e.g., `feat/pi-payment-ui`, `fix/auth-error-handling`):
     ```bash
     git checkout -b branch-name
     ```

2. **Make Changes**:
   - Follow the [Coding Standards](#coding-standards).
   - Commit with clear messages:
     ```bash
     git commit -m "feat: add payment status UI to auth page"
     ```

3. **Push and Open a PR**:
   - Push your branch:
     ```bash
     git push origin branch-name
     ```
   - Create a pull request (PR) against the `main` branch of the TruthWeb repo.
   - Link related issues (e.g., "Fixes #12").

4. **Review Process**:
   - Respond to feedback from maintainers.
   - Ensure your code works in the Pi Browser sandbox.

5. **Merge**:
   - Once approved, your changes will be merged!

---

## Development Guidelines

### Coding Standards
- **JavaScript**:
  - Use ES6+ (e.g., `const`, `let`, arrow functions).
  - Follow [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript).
  - Indent with 2 spaces.
  - Comment complex logic for clarity.
- **HTML/CSS**:
  - Use semantic HTML5 tags.
  - Leverage Tailwind CSS classes consistently (as in `auth.html`).
  - Keep styles in `<style>` or separate CSS files.
- **File Naming**: Lowercase with hyphens (e.g., `auth.js`, `payment-route.js`).
- **Commits**: Use [Conventional Commits](https://www.conventionalcommits.org/):
  - `feat`: New feature (e.g., "feat: add profile link after auth").
  - `fix`: Bug fix (e.g., "fix: handle missing username").
  - `docs`: Documentation updates.

### Testing
- **Backend**:
  - Test API endpoints with Postman or curl:
    ```bash
    curl -X POST http://localhost:3000/auth/pi -H "Content-Type: application/json" -d '{"accessToken":"test","user":{"uid":"123","username":"testuser"}}'
    ```
  - Add unit tests with Jest if contributing significant logic (optional for now).
- **Frontend**:
  - Test in Pi Browser (sandbox mode).
  - Verify UI updates (e.g., "Authenticated as [username]").
  - Check console for errors during authentication.
- Include test results in your PR if applicable.

---

## Community
Join the TruthWeb community to connect with other contributors:
- **Telegram**: [TruthWebOfficial](https://t.me/TruthWebOfficial)
- **Twitter/X**: [@reimagine_truth](https://x.com/reimagine_truth)
- **GitHub Discussions**: (Add link if enabled)

Your feedback and ideas help shape TruthWeb’s future!

---

## Contact
For questions or support:
- Open an issue on GitHub.
- Email: [truthweb.support@example.com](mailto:truthweb.support@example.com) (replace with actual email).
- Chat with us on Telegram or other community channels.

Thank you for contributing to TruthWeb! Together, we’re reimagining the web for the Pi Network community.
