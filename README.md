# 🧾 Open-Source Receipt Templates (HTML & CSS)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](index.html)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](styles/receipts.css)
[![Live Demo](https://img.shields.io/badge/GitHub_Pages-Live_Demo-success)](https://hanshan0228.github.io/receipt-templates/)
[![Online Receipt Maker](https://img.shields.io/badge/Interactive_Generator-receiptnumber.com-10b981)](https://receiptnumber.com)

A clean, production-grade collection of **10 zero-dependency HTML & CSS printable receipt templates** designed for small businesses, freelancers, landlords, retail stores, restaurants, and medical practices.

Every template is 100% printable, responsive, and customizable without React, Vue, build steps, or external dependencies.

🌐 **Interactive Live Gallery & Print Preview**: [https://hanshan0228.github.io/receipt-templates/](https://hanshan0228.github.io/receipt-templates/)

> 💡 **Looking for an interactive web builder?**  
> If you need automated calculations, sequential receipt numbering, customizable currency symbols ($/€/£/¥), company logo uploads, and one-click PDF or Excel downloads, visit the free **[ReceiptNumber - Online Receipt Maker & Generator](https://receiptnumber.com)**.

---

## 📑 Table of Contents

- [Included Templates](#-included-templates)
- [Live Gallery & Demo](#-live-gallery--demo)
- [Developer Quick Start](#-developer-quick-start)
- [JSON Data Schema Example](#-json-data-schema-example)
- [Print & PDF Export Guidelines](#-print--pdf-export-guidelines)
- [IRS & Tax Audit Compliance](#-irs--tax-audit-compliance)
- [Format Downloads (Word & Excel)](#-format-downloads-word--excel)
- [Plantillas en Español (Modelos de Recibo)](#-plantillas-en-español-modelos-de-recibo)
- [SEO & Resource Directory](#-seo--resource-directory)
- [License](#-license)

---

## 📦 Included Templates

| Template File | Category | Description | Live Builder |
|---|---|---|---|
| [`templates/thermal-80mm.html`](templates/thermal-80mm.html) | POS & Retail | Standard 80mm/58mm thermal paper roll slip for retail, grocery, and coffee shops. | [Create Thermal Receipt](https://receiptnumber.com) |
| [`templates/restaurant-guest-check.html`](templates/restaurant-guest-check.html) | Dining & Cafe | Itemized guest check with food/drink subtotal, state taxes, tip guide, and signature line. | [Make Restaurant Receipt](https://receiptnumber.com) |
| [`templates/rent-receipt.html`](templates/rent-receipt.html) | Real Estate | Official monthly tenant payment acknowledgment with lease term, property address, and balance due. | [Generate Rent Receipt](https://receiptnumber.com/templates/rent-receipt) |
| [`templates/cash-receipt.html`](templates/cash-receipt.html) | General Service | Legally binding cash payment voucher with spelled-out amount, payee, and contractor signature. | [Make Cash Receipt](https://receiptnumber.com/templates/cash-receipt) |
| [`templates/donation-charity-receipt.html`](templates/donation-charity-receipt.html) | Non-Profit | Official 501(c)(3) tax deduction receipt with required IRS IRC § 170 substantiation statement. | [Make Donation Receipt](https://receiptnumber.com/receipt-template/word) |
| [`templates/gas-station-receipt.html`](templates/gas-station-receipt.html) | Travel & Auto | Pump fuel voucher with price per gallon, fuel taxes, and odometer mileage reimbursement log. | [Generate Gas Receipt](https://receiptnumber.com/templates/gas-station-receipt) |
| [`templates/taxi-cab-receipt.html`](templates/taxi-cab-receipt.html) | Travel & Auto | Meter fare breakdown, airport tolls, and tip calculation for corporate expense filing. | [Travel Mileage Tools](https://receiptnumber.com/templates/gas-station-receipt) |
| [`templates/hotel-folio-receipt.html`](templates/hotel-folio-receipt.html) | Hospitality | Itemized lodging folio with room night rates, occupancy taxes, room service, and zero-balance audit. | [Excel Lodging Tracker](https://receiptnumber.com/receipt-template/excel) |
| [`templates/medical-doctor-receipt.html`](templates/medical-doctor-receipt.html) | Healthcare | Clinical visit CPT codes, insurance adjustment deductions, and patient copay receipt for HSA/FSA claims. | [Healthcare Expense Tools](https://receiptnumber.com) |
| [`templates/recibo-de-pago-es.html`](templates/recibo-de-pago-es.html) | Multilingual | Plantilla oficial en español de constancia de entrega de dinero con base imponible, IVA y firmas. | [Modelo Recibo Español](https://receiptnumber.com/es/recibo-de-pago) |

---

## 🌐 Live Gallery & Demo

You can preview and test-print all templates directly in your browser:

1. **Online Web Preview**: Visit [https://hanshan0228.github.io/receipt-templates/](https://hanshan0228.github.io/receipt-templates/)
2. **Local Preview**:
   ```bash
   git clone https://github.com/hanshan0228/receipt-templates.git
   cd receipt-templates
   open index.html # macOS
   # or on Linux / Windows:
   python3 -m http.server 8080
   ```

---

## 💻 Developer Quick Start

### 1. Minimal HTML Embedding
All layouts depend only on `styles/receipts.css`:

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="styles/receipts.css">
</head>
<body>
  <div class="receipt-card receipt-thermal">
    <div class="receipt-header">
      <h1>ACME COFFEE LAB</h1>
      <div class="receipt-meta">Store #101 • San Francisco, CA</div>
    </div>
    <div class="receipt-divider"></div>
    <table class="receipt-table">
      <tr><td>Pour Over (Ethiopia)</td><td class="num">1</td><td class="num">$6.50</td></tr>
    </table>
    <div class="receipt-totals">
      <div class="receipt-row grand-total"><span>TOTAL</span><span>$6.50</span></div>
    </div>
  </div>
</body>
</html>
```

---

## 📄 JSON Data Schema Example

Integrating into a Node.js, Python, or Go microservice? Here is the canonical data structure matching these templates:

```json
{
  "receiptNumber": "RN-2026-8492",
  "date": "2026-02-11T14:32:00Z",
  "currency": "USD",
  "merchant": {
    "name": "Metro Retail Store",
    "address": "742 Evergreen Terrace, Springfield, OR 97477",
    "phone": "(555) 019-2834",
    "taxId": "US-84-9201948"
  },
  "items": [
    { "description": "Organic Arabica Coffee 12oz", "quantity": 1, "unitPrice": 14.50, "total": 14.50 },
    { "description": "Stainless Travel Tumbler", "quantity": 1, "unitPrice": 24.00, "total": 24.00 }
  ],
  "subtotal": 38.50,
  "taxRate": 0.0725,
  "taxAmount": 2.79,
  "total": 41.29,
  "paymentMethod": "Visa Debit (**** 4821)"
}
```

---

## 🖨️ Print & PDF Export Guidelines

All templates include dedicated `@media print` CSS definitions:
- Thermal templates are sized to 80mm (3.15in) roll width.
- Navigation toolbars, test buttons, and page backgrounds are hidden automatically (`.no-print`).
- Prevents page breaks within receipt cards (`page-break-inside: avoid`).

**How to export crisp PDFs in Chrome, Safari, or Edge:**
1. Press `Ctrl + P` (or `Cmd + P` on macOS).
2. Set **Destination** to **Save as PDF** (or select your ESC/POS thermal printer).
3. Set **Margins** to **None** or **Minimum**.
4. Check **Background graphics** if you wish to retain subtle badge colors.

---

## ⚖️ IRS & Tax Audit Compliance

Looking to verify whether digital or generated receipts satisfy tax authorities during an audit?

Read our comprehensive guide: **[IRS Business Expense Receipt Requirements (Small Business Guide)](docs/irs-receipt-requirements.md)**
- **IRC § 274 Compliance**: The 5 required fields for valid business deductions.
- **The $75 Rule**: When receipts are strictly required vs. when contemporaneous logs suffice.
- **IRS Rev. Proc. 97-22**: Legal validity of electronic and PDF receipts.

---

## 📊 Format Downloads (Word & Excel)

Need offline spreadsheets or Word documents with pre-built math formulas?

- 📗 **[Excel Receipt Templates (.xlsx)](https://receiptnumber.com/receipt-template/excel)** — Automated `SUM` formulas, sales tax multipliers, and formatted print areas.
- 📘 **[Word Receipt Templates (.docx)](https://receiptnumber.com/receipt-template/word)** — Editable Microsoft Word tables with form fields and modern typography.

---

## 🇪🇸 Plantillas en Español (Modelos de Recibo)

Colección de plantillas descargables e imprimibles para autónomos y pequeñas empresas:

- **[Modelo de Recibo de Pago](https://receiptnumber.com/es/recibo-de-pago)**: Justificante legal de entrega de dinero en efectivo o transferencia.
- **[Recibo de Dinero en Efectivo](https://receiptnumber.com/es/recibo-de-pago)**: Comprobante con desglose de IVA y firmas de emisor y receptor.
- **[Recibo de Alquiler / Renta](https://receiptnumber.com/es/recibo-de-pago)**: Justificante de pago mensual para inquilinos y propietarios.

---

## 🔍 SEO & Resource Directory

- **[Free Receipt Maker](https://receiptnumber.com)**: Online receipt creator with instant PDF export.
- **[Online Receipt Generator](https://receiptnumber.com)**: Custom numbering, multi-currency support, and logo branding.
- **[Rent Receipt Template](https://receiptnumber.com/templates/rent-receipt)**: Proof of payment for apartment tenants and leases.
- **[Cash Receipt Template](https://receiptnumber.com/templates/cash-receipt)**: Formal acknowledgment for cash transactions.
- **[Gas Station Receipt](https://receiptnumber.com/templates/gas-station-receipt)**: Fuel purchase records for IRS / CRA business mileage deductions.

---

## 📄 License

This repository is licensed under the [MIT License](LICENSE) — free for personal, commercial, and educational use.

Maintained with ❤️ by the open-source community and **[ReceiptNumber](https://receiptnumber.com)**.
