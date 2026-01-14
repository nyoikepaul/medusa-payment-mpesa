# 🇰🇪 MedusaJS M-Pesa Payment Provider

[![Medusa Version](https://img.shields.io/badge/Medusa-v2.0--compatible-orange?style=flat-square)](https://medusajs.com/)
[![Language](https://img.shields.io/badge/Language-TypeScript-blue?style=flat-square)](https://www.typescriptlang.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

A specialized payment module for [MedusaJS](https://medusajs.com/) that enables Kenyan merchants to accept mobile money via **Safaricom M-Pesa**. This plugin implements the **Daraja 2.0 API** for a seamless, secure, and automated checkout experience.

---

## 🚀 Features

- **Lipa Na M-Pesa Online (STK Push):** Triggers an instant PIN prompt on the customer's mobile device.
- **Asynchronous Webhooks:** Securely processes payment results via Safaricom's callback system.
- **Idempotency Support:** Prevents duplicate transactions for the same order.
- **Payment Reconciliation:** Automatically updates Medusa's `PaymentStatus` to `captured` upon successful M-Pesa confirmation.
- **Refund Support:** (Coming Soon) Initiation of M-Pesa reversals directly from the Medusa Admin Dashboard.

## 🏗️ Architecture & Workflow



1. **Initiation:** When a customer selects M-Pesa at checkout, Medusa calls this provider.
2. **STK Push:** The provider sends a request to the Daraja API to trigger a prompt on the user's phone.
3. **Wait State:** The order remains in a "Pending" state in Medusa.
4. **Callback:** Safaricom sends a POST request to our webhook endpoint with the transaction results.
5. **Completion:** The plugin validates the result and marks the order as paid.

## 🛠️ Installation

1. **Install the plugin via npm:**
   ```bash
   npm install medusa-payment-mpesa
