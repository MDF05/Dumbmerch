# Contributing to dumbmerch

Thank you for your interest in contributing to **dumbmerch**! We welcome contributions from everyone, whether it's bug reports, feature requests, documentation improvements, or code changes.

## 📋 Table of Contents
- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Pull Requests](#pull-requests)
- [Development Workflow](#development-workflow)
- [Style Guide](#style-guide)

## 🤝 Code of Conduct

This project and everyone participating in it is governed by the [Code of Conduct](./CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## 🚀 How to Contribute

### Reporting Bugs
If you find a bug, please check the [Issue Tracker](../../issues) to see if it has already been reported. If not, please open a new issue with:
- A clear title.
- Steps to reproduce.
- Expected vs actual behavior.
- Screenshots or logs if applicable.

### Suggesting Enhancements
We love new ideas! detailed RFCs (Request for Comments) are encouraged for major changes. Open an issue with the **enhancement** label.

### Pull Requests
1. **Fork the repo** and create your branch from `main` (or the relevant development branch).
   ```bash
   git checkout -b feature/my-amazing-feature
   ```
2. **Install dependencies** and ensure everything runs locally.
3. **Make your changes**.
4. **Test your changes**.
5. **Ensure your code follows the style guide**.
6. **Commit** with a descriptive message.
   ```bash
   git commit -m "feat: add user profile page" 
   ```
   (We recommend [Conventional Commits](https://www.conventionalcommits.org/))
7. **Push** to your fork.
8. **Open a Pull Request**!

## 💻 Development Workflow

1. **Setup**: Refer to the [Getting Started](./README.md#getting-started) section.
2. **Branching**: Use feature branches. Do not push directly to `main`.
3. **Syncing**: Keep your fork in sync with the upstream repository.

## 🎨 Style Guide

### General
- Use clear and meaningful variable names.
- Comment complex logic, but aim for self-documenting code.
- Write strict TypeScript. Avoid `any` whenever possible.

### Frontend (React)
- Use Functional Components and Hooks.
- Place components in their own folders if they have associated styles/tests.
- Use Chakra UI / Tailwind tokens instead of hardcoded hex values.

### Backend (Node/Express)
- Follow the Controller-Service pattern.
- Validate all inputs using Zod.
- Handle errors gracefully using a global error handler.

## ❓ Getting Help

Join our community or check [SUPPORT.md](./SUPPORT.md) for help.
