# 🇰🇪 MedusaJS M-Pesa Payment Provider

[![Medusa Plugin](https://img.shields.io/badge/Medusa-Plugin-orange?style=flat-square)](https://medusajs.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A high-performance payment provider for [MedusaJS](https://medusajs.com/) that integrates **Safaricom M-Pesa (Daraja API)**. This plugin enables Kenyan merchants to accept mobile money payments via STK Push directly on their storefront.

---

## 🚀 Key Features
- **STK Push (Lipa Na M-Pesa Online):** Triggers an immediate PIN prompt on the customer's phone.
- **Real-time Callbacks:** Securely handles transaction confirmation via Safaricom webhooks.
- **Automatic Reconciliation:** Automatically marks Medusa orders as "Paid" upon successful transaction.
- **Sandbox & Production Ready:** Easily toggle between Safaricom's testing environment and live credentials.

## 🛠️ Technical Stack
- **Backend:** Node.js, TypeScript
- **Framework:** MedusaJS (Commerce Engine)
- **API:** Safaricom Daraja API (REST)

## 📦 Installation

1. **Install the package:**
   ```bash
   npm install medusa-payment-mpesa
