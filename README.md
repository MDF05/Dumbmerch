# dumbmerch

> **Enterprise-Grade Monorepo for Scalable E-Commerce Solutions**

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Version](https://img.shields.io/badge/version-1.0.0-blue)

## 📖 Project Overview

**dumbmerch** is a modern, full-stack monorepo designed to deliver a robust and scalable e-commerce experience. It unifies a high-performance frontend built with React and Vite, and a reliable, type-safe backend powered by Node.js, Express, and Prisma.

This repository serves as the central hub for development, containing all services and client applications required to run the platform.

### Key Features
- **Modern Tech Stack**: Leveraging the latest stable versions of React, TypeScript, and Node.js.
- **Monorepo Structure**: Centralized code management for better developer ergonomics.
- **Type Safety**: End-to-end TypeScript integration.
- **Scalable Architecture**: Designed with modularity and separation of concerns in mind.

---

## 🏗 Repository Structure

This is a **ROOT / MONOREPO** repository containing the following sub-projects:

| Directory | Service | Description |
| :--- | :--- | :--- |
| [`/backend-dumbmerch`](https://github.com/MDF05/Dumbmerch-Backend) | **Backend API** | RESTful API service handling business logic, database interactions, and authentication. |
| [`/frontend-dumbmerch`](https://github.com/MDF05/Dumbemerch-Frontend) | **Frontend Client** | Responsive web application provided user interface for customers and admins. |

---

## 📚 Documentation

The following documentation is available to guide you through the project's architecture, governance, and usage.

### Core Documentation
- [**📖 ARCHITECTURE.md**](./ARCHITECTURE.md) - System architecture, boundaries, and communication patterns.
- [**🗺 ROADMAP.md**](./ROADMAP.md) - Future plans, upcoming features, and milestones.
- [**📝 CHANGELOG.md**](./CHANGELOG.md) - Detailed history of changes and version releases.

### Community & Governance
- [**🤝 CONTRIBUTING.md**](./CONTRIBUTING.md) - Guidelines for contributing code, reporting issues, and submitting PRs.
- [**⚖️ GOVERNANCE.md**](./GOVERNANCE.md) - Decision-making processes and project maintainers.
- [**❤️ CODE_OF_CONDUCT.md**](./CODE_OF_CONDUCT.md) - Standards for community behavior and interaction.

### Legal & Safety
- [**🛡 SECURITY.md**](./SECURITY.md) - Security policies and vulnerability reporting.
- [**⚠️ DISCLAIMER.md**](./DISCLAIMER.md) - Project usage disclaimers and liabilities.
- [**📜 LICENSE**](./LICENSE) - Licensing details (MIT).

### Support
- [**🆘 SUPPORT.md**](./SUPPORT.md) - How to get help and support channels.

### Sub-Project Documentation
- [**Backend Documentation**](https://github.com/MDF05/Dumbmerch-Backend/blob/main/README.md)
- [**Frontend Documentation**](https://github.com/MDF05/Dumbemerch-Frontend/blob/main/README.md)

---

## 🚀 Getting Started

### Prerequisites
- **Node.js**: >= 18.x
- **npm** or **yarn** or **pnpm**
- **PostgreSQL**: Local instance or remote URL
- **Git**

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/MDF05/dumbmerch.git
   cd dumbmerch
   ```

2. **Install Dependencies**
   It is recommended to install dependencies for root (if any) and individual sub-projects.
   ```bash
   # Backend
   cd backend-dumbmerch
   npm install

   # Frontend
   cd ../frontend-dumbmerch
   npm install
   ```

3. **Environment Setup**
   Copy `.env.example` to `.env` in both `backend-dumbmerch` and `frontend-dumbmerch` directories and populate with necessary credentials (DB URL, API keys, etc.).

4. **Running Locally**
   
   *Terminal 1 - Backend:*
   ```bash
   cd backend-dumbmerch
   npm run dev
   ```

   *Terminal 2 - Frontend:*
   ```bash
   cd frontend-dumbmerch
   npm run dev
   ```

---

## 🛠 Tech Stack

### Backend (`/backend-dumbmerch`)
- **Runtime**: Node.js
- **Framework**: Express.js
- **Language**: TypeScript
- **ORM**: Prisma
- **Database**: PostgreSQL (Primary)
- **Validation**: Zod
- **Documentation**: Swagger UI
- **Real-time**: Socket.io / WS
- **Payment**: Midtrans
- **Image Storage**: Cloudinary

### Frontend (`/frontend-dumbmerch`)
- **Framework**: React.js
- **Build Tool**: Vite
- **Language**: TypeScript
- **Styling**: Chakra UI, TailwindCSS, Emotion
- **State Management**: Redux Toolkit
- **Forms**: React Hook Form, Formik
- **Animations**: Framer Motion
- **Networking**: Axios

---

## 🤝 Contribution Flow

We welcome contributions! Please see our [CONTRIBUTING.md](./CONTRIBUTING.md) for details on how to get started.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 🛡 Security

For security concerns, please refer to [SECURITY.md](./SECURITY.md). Do not report vulnerabilities in public issues.

---

## 👥 Maintainers

- **Dava** - *Project Lead* - [Profile](https://github.com/MDF05)

---

## 📄 License

Distributed under the MIT License. See [LICENSE](./LICENSE) for more information.
