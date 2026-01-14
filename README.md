# 🇰🇪 ERPNext Kenya Tax Compliance (eTIMS)

[![Frappe App](https://img.shields.io/badge/Frappe-App-blue?style=flat-square)](https://frappeframework.com/)
[![KRA eTIMS](https://img.shields.io/badge/KRA-eTIMS--Ready-green?style=flat-square)](https://www.kra.go.ke/)

This Frappe/ERPNext application provides a seamless integration between your ERP system and the **Kenya Revenue Authority (KRA) eTIMS** platform. It automates the legal requirement of transmitting electronic tax invoices via the Virtual Sales Control Unit (VSCU) or Online Sales Control Unit (OSCU).

---

## 🚀 Key Features
- **Real-time Invoicing:** Automatically pushes Sales Invoices to eTIMS upon submission in ERPNext.
- **QR Code Generation:** Fetches the unique KRA signature and embeds the mandatory QR code on print formats.
- **Item Synchronization:** Maps ERPNext item codes to KRA's HS Codes/UNSPSC standards.
- **Error Logs & Reconciliation:** Tracks failed transmissions with detailed KRA response codes for easy troubleshooting.
- **Credit/Debit Note Support:** Full compliance for adjustments and returns.

## 🛠️ Technical Stack
- **Framework:** Frappe Framework (Python/JS)
- **Base App:** ERPNext
- **API:** KRA GavaConnect / eTIMS VSCU API

## 📦 Installation

To install this module on your Frappe bench:

```bash
bench get-app [https://github.com/nyoikepaul/erpnext-kenya-compliance](https://github.com/nyoikepaul/erpnext-kenya-compliance)
bench --site [your-site-name] install-app erpnext-kenya-compliance
bench migrate
