# 🇰🇪 WooCommerce Kenya Bridge (M-Pesa & Logistics)

[![WooCommerce](https://img.shields.io/badge/WooCommerce-Framework-purple?style=flat-square)](https://woocommerce.com/)
[![M-Pesa](https://img.shields.io/badge/Safaricom-M--Pesa-green?style=flat-square)](https://developer.safaricom.co.ke/)

The standard WooCommerce setup doesn't account for the unique landscape of Kenyan e-commerce. This "Bridge" repository provides the custom logic needed to integrate **Lipa Na M-Pesa** and **Zone-based Shipping** for local courier services.

---

## 🚀 Key Modules

### 1. M-Pesa Express (STK Push) Gateway
Custom PHP implementation that triggers a payment prompt on the customer's phone at checkout.
- **Auto-Verification:** Uses Daraja API callbacks to verify payments instantly.
- **Manual Check:** Provides a fallback "Verify Payment" button in the Admin dashboard for manual reconciliation.

### 2. Kenyan Logistics & Shipping Calculator
Pre-configured zones for major Kenyan towns (Nairobi, Mombasa, Kisumu, Nakuru, etc.).
- **Courier Integration:** Logic to calculate rates for **G4S**, **Fargo Courier**, and **Sendy**.
- **Pick-up Points:** Support for "Collect at Courier Office" vs. "Door-to-Door" delivery options.

## 🛠️ Technical Implementation
- **Hooks & Filters:** Uses standard WooCommerce hooks (`woocommerce_payment_gateways`, `woocommerce_shipping_methods`) to ensure compatibility with any WordPress theme.
- **REST API:** Handles incoming webhooks from Safaricom and Sendy securely.
- **AJAX Checkout:** Smooth, no-refresh experience when a user selects their delivery sub-county.

## 📦 How to Use
1. Clone this into your `/wp-content/plugins/` directory.
2. In WordPress Admin, go to **WooCommerce > Settings > Payments** to enable M-Pesa.
3. Go to **WooCommerce > Settings > Shipping** to configure town-based rates.

## 💼 For Upwork Clients
I provide end-to-end e-commerce setup for the Kenyan market, including:
- **Custom Plugin Development**
- **Tax (VAT) Configuration**
- **M-Pesa B2C (Disbursements) for vendor payouts**

---
**Developed by [Nyoike Paul](https://github.com/nyoikepaul)** *Building high-conversion e-commerce for the 254.*
