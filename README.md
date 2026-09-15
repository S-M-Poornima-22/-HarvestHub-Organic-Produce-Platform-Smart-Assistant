

<div align="center">

# 🌿 HarvestHub — Organic Produce & Contextual AI Assistant

**A responsive e-commerce web platform engineered for fresh farm produce tracking, real-time cart state management, and contextual AI-driven customer assistance.**

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-2.x-000000?style=flat&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

[Key Features](#-key-features) • [System Architecture](#-system-architecture) • [API Reference](#-api-endpoints) • [Quickstart](#-installation--local-setup)

</div>

---

## 📌 Problem & Motivation

Access to fresh, organic farm produce often suffers from supply transparency issues and friction during customer checkout. Consumers struggle to verify harvest cycles, origin farms, and nutritional freshness before purchase. 

**HarvestHub** bridges this gap by combining:
1. An accessible, responsive client storefront with dynamic local cart persistence.
2. A lightweight **Flask microservice backend** managing product inventories and farm origin metadata.
3. An integrated **Contextual AI Chatbot** answering instant queries on product availability, harvest schedules, and cooking profiles.

---

## ✨ Key Features

* **Dynamic Cart State Engine:** Zero-latency client-side cart updates with persistent storage synchronization.
* **Contextual AI Produce Assistant:** Lightweight backend conversational service resolving queries about shelf life, origin farms, and order guidance.
* **Traceable Produce Catalog:** Detailed data cards showcasing harvest timestamps, certification tags, and batch quantities.
* **Responsive Viewport Design:** Built mobile-first with CSS Grid and semantic HTML5 to support fluid shopping across devices.
* **Lightweight REST Endpoints:** Clean JSON responses for product queries, search filtering, and support dialog.

---

## 🏗️ System Architecture

```text
[ Client Browser (ES6+ / Fetch API / CSS3) ]
                   │
                   ▼  HTTPS / JSON
[ Flask Microservice Backend (Python) ]
     ├── /api/v1/products   ──> [ Inventory & Origin Service ]
     ├── /api/v1/cart       ──> [ Session / State Handler ]
     └── /api/v1/assistant  ──> [ Context Query Engine / NLP ]
