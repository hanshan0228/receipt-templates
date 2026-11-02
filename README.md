# 🧾 Open-Source Receipt Templates (HTML & CSS)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](index.html)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](styles/receipts.css)
[![Live Demo](https://img.shields.io/badge/GitHub_Pages-Live_Demo-success)](https://hanshan0228.github.io/receipt-templates/)
[![Online Receipt Maker](https://img.shields.io/badge/Interactive_Generator-receiptnumber.com-10b981)](https://receiptnumber.com)

A clean, lightweight collection of **zero-dependency HTML & CSS receipt templates** designed for small businesses, freelancers, landlords, retail stores, and restaurants. Every template is 100% printable, responsive, and customizable.

🌐 **Live Interactive Gallery & Print Preview**: [https://hanshan0228.github.io/receipt-templates/](https://hanshan0228.github.io/receipt-templates/)

> 💡 **Looking for an interactive web builder?**  
> If you need auto-calculated totals, sequential receipt numbers, currency toggles, or instant PDF/Excel exports, visit the free **[ReceiptNumber - Online Receipt Maker & Generator](https://receiptnumber.com)**.

---

## 📑 Table of Contents

- [Included Templates](#-included-templates)
- [Live Gallery & Demo](#-live-gallery--demo)
- [Keyword & Template Directory](#-keyword--template-directory)
- [Quick Start Guide](#-quick-start-guide)
- [Customization & Print Settings](#-customization--print-settings)
- [Format Downloads (Word & Excel)](#-format-downloads-word--excel)
- [Plantillas en Español (Modelos de Recibo)](#-plantillas-en-español-modelos-de-recibo)
- [License](#-license)

---

## 📦 Included Templates

| Template File | Category | Description | Live Builder |
|---|---|---|---|
| [`templates/thermal-80mm.html`](templates/thermal-80mm.html) | POS & Retail | Standard 80mm/58mm thermal paper roll slip for retail, grocery, and coffee shops. | [Create Thermal Receipt](https://receiptnumber.com) |
| [`templates/restaurant-guest-check.html`](templates/restaurant-guest-check.html) | Dining & Cafe | Itemized guest check with food/drink subtotal, state taxes, tip guide, and signature line. | [Make Restaurant Receipt](https://receiptnumber.com) |
| [`templates/rent-receipt.html`](templates/rent-receipt.html) | Real Estate | Official monthly tenant payment acknowledgment with lease term, property address, and balance due. | [Generate Rent Receipt](https://receiptnumber.com/templates/rent-receipt) |
| [`templates/cash-receipt.html`](templates/cash-receipt.html) | General Service | Legally binding cash payment voucher with spelled-out amount, payee, and contractor signature. | [Make Cash Receipt](https://receiptnumber.com/templates/cash-receipt) |
| [`templates/gas-station-receipt.html`](templates/gas-station-receipt.html) | Travel & Auto | Pump fuel voucher with price per gallon, fuel taxes, and odometer mileage reimbursement log. | [Generate Gas Receipt](https://receiptnumber.com/templates/gas-station-receipt) |

---

## 🌐 Live Gallery & Demo

You can preview all templates directly in your browser without any build tools or dependencies:

1. Clone the repository:
   ```bash
   git clone https://github.com/hanshan0228/receipt-templates.git
   cd receipt-templates
   ```
2. Open `index.html` in any web browser:
   ```bash
   open index.html # macOS
   # or start a quick local server:
   npx serve .
   ```

---

## 🔍 Keyword & Template Directory

Whether you are building an e-commerce checkout flow, a point-of-sale (POS) terminal, or filing small business expense reports, here are direct resources:

- **[Free Receipt Maker](https://receiptnumber.com)**: Browser-based invoice and receipt generation with no sign-up required.
- **[Online Receipt Generator](https://receiptnumber.com)**: Generate custom receipts with company logos, VAT/sales tax rules, and receipt numbering.
- **[Rent Receipt Template](https://receiptnumber.com/templates/rent-receipt)**: Proof of payment for apartment tenants, commercial leases, and room sublets.
- **[Cash Receipt Template](https://receiptnumber.com/templates/cash-receipt)**: Protect cash payments for freelance services, equipment sales, and informal transactions.
- **[Gas Station Receipt](https://receiptnumber.com/templates/gas-station-receipt)**: Itemized fuel purchase records for IRS / CRA business mileage deductions.

---

## 🚀 Quick Start Guide

### 1. Standalone HTML Embedding
Simply include `styles/receipts.css` in your project:

```html
<link rel="stylesheet" href="styles/receipts.css">

<div class="receipt-card receipt-thermal">
  <div class="receipt-header">
    <h1>YOUR BUSINESS NAME</h1>
    <div class="receipt-meta">123 Market St • (555) 000-1234</div>
  </div>
  <!-- Insert receipt items -->
</div>
```

### 2. Print & PDF Generation (`@media print`)
All templates feature optimized `@media print` rules:
- Removes extraneous backgrounds and utility buttons (`.no-print`).
- Locks paper width to standard receipt roll sizes (80mm / 3.15in).
- Prevents page breaks within receipt cards (`page-break-inside: avoid`).

To print or save as PDF in Chrome or Edge:
1. Press `Ctrl + P` (or `Cmd + P` on macOS).
2. Under **Destination**, select **Save as PDF** or pick your connected POS Thermal Printer (Epson, Star Micronics, Munbyn).
3. Under **Margins**, choose **None** or **Minimum**.

---

## 📊 Format Downloads (Word & Excel)

Prefer desktop spreadsheet and document software for your accounting team? Download free pre-formatted templates:

- 📗 **[Excel Receipt Templates (.xlsx)](https://receiptnumber.com/receipt-template/excel)** — Automated SUM formulas, tax rates, and printable A4/Letter sheets.
- 📘 **[Word Receipt Templates (.docx)](https://receiptnumber.com/receipt-template/word)** — Editable tables with fillable form fields and clean typographic styles.

---

## 🇪🇸 Plantillas en Español (Modelos de Recibo)

Para usuarios y empresas hispanohablantes en España, México, Colombia, Argentina y Estados Unidos:

- **[Modelo de Recibo de Pago](https://receiptnumber.com/es/recibo-de-pago)**: Formato estándar para constancia de pago de servicios y productos.
- **[Recibo de Dinero en Efectivo](https://receiptnumber.com/es/recibo-de-pago)**: Comprobante legal de entrega de dinero con firma y concepto.
- **[Recibo de Alquiler / Renta](https://receiptnumber.com/es/recibo-de-pago)**: Justificante de mensualidad de arrendamiento para inquilinos y propietarios.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — you are free to use, modify, and distribute these templates in commercial or private projects.

Maintained with ❤️ by **[ReceiptNumber](https://receiptnumber.com)**.
