# 🌐 Nexus CMS — Professional Community Management System

<p align="center">
  <img width="100%" alt="Nexus CMS System Architecture" src="https://github.com/user-attachments/assets/ab19bc60-5487-4c44-9100-2be5bda339a4" />
</p>

<p align="center">
  <b>A high-performance, full-stack CMS for modern digital communities.</b><br/>
  Manage users, content, and media from a centralized, secure admin dashboard.
</p>

<p align="center">
  <a href="#-project-overview">Overview</a> •
  <a href="#-key-features">Features</a> •
  <a href="#-technical-architecture">Architecture</a> •
  <a href="#-project-structure">Structure</a> •
  <a href="#-installation--setup">Setup</a> •
  <a href="#-roadmap">Roadmap</a> •
  <a href="#-license">License</a>
</p>

---

## 📖 Project Overview

**Nexus CMS** is a robust Content Management System engineered to provide a centralized dashboard for administrators to:

- Manage users and roles
- Curate digital content (blogs, announcements, pages)
- Upload and serve high-resolution media assets securely

By using a **Decoupled Data Strategy**, Nexus CMS separates:

- **Content & metadata** → MongoDB Atlas  
- **Media delivery** → Firebase Cloud Storage  

This enables **high availability** and **fast load times**, even for media-heavy communities.

---

## 🚀 Key Features

### 🛠️ Administrative Governance

- **Role-Based Access Control (RBAC):** Tiered permissions for **Admins**, **Moderators**, and **Members**
- **Dynamic Dashboard:** Real-time insights on user growth, activity, and engagement
- **Full CRUD Engine:** Manage blogs, announcements, and pages with status tracking:
  - `Draft` → `Published` → `Archived`

### 📁 Scalable Infrastructure

- **Hybrid Storage:** Metadata in MongoDB Atlas + media in Firebase Storage
- **Stateless Auth:** JWT-based authentication for scalable, cross-platform deployments
- **SEO Optimized:** Server-side rendered Handlebars (HBS) templates for fast indexing

---

## 🏗️ Technical Architecture

This project follows a modern **MVC (Model–View–Controller)** approach:

- **View Layer:** Handlebars templates + CSS3 (Flex/Grid) + Vanilla JS
- **Logic Layer:** Node.js / Express middleware for:
  - validation
  - auth guards
  - business logic
- **Data Layer:** Mongoose schemas for strict validation and relationships
- **External Integration:** Firebase Admin SDK for secure media handling and delivery

---

## 📂 Project Structure

```txt
.
├── config/             # Database & Firebase service connections
├── controllers/        # Controllers for route logic
├── middleware/         # Auth guards & role validation
├── models/             # Mongoose models (User, Post, Community)
├── public/             # Static assets (CSS, images, client-side JS)
├── routes/             # API + view route definitions
├── views/              # Handlebars (HBS) template files
└── app.js              # Application entry point & configuration
```

---

## 🛠️ Installation & Setup

### 1) Prerequisites

- **Node.js** `v16+`
- **MongoDB Atlas** account + cluster
- **Firebase** project credentials

### 2) Clone & Install

```bash
git clone https://github.com/rajkandula/CMS.git
cd CMS
npm install
```

### 3) Environment Variables

Create a `.env` file in the root directory:

```env
PORT=3000
MONGO_URI=your_mongodb_atlas_connection_string
FIREBASE_API_KEY=your_firebase_key
JWT_SECRET=your_super_secret_string
```

> Tip: Never commit `.env` to GitHub. Add it to `.gitignore`.

### 4) Run the Application

```bash
# Development mode
npm run dev

# Production mode
npm start
```

---

## 📈 Roadmap

- [ ] **Socket.io Integration:** Real-time chat and live community notifications
- [ ] **Advanced Search:** Integrate Algolia for instant content filtering
- [ ] **REST API Docs:** Swagger / OpenAPI for developer access
- [ ] **Analytics Suite:** Heatmaps and engagement tracking for admins

---

## 🤝 Contributing

Contributions are welcome!

- Open an issue for bugs/feature requests
- Submit a PR with clear context and screenshots when relevant

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.

---

## 👤 Maintainer

**Charan Raj Kandula**
