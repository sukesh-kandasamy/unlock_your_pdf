# 🔓 PDF Unlocker

A **100% client-side** web application that removes password protection from PDF files — entirely within your browser. No file uploads, no servers, completely private.

---

## 📖 Overview

PDF Unlocker is a single-page HTML tool that allows users to decrypt password-protected PDF files without sending any data to a server. The entire decryption process runs locally in the browser using JavaScript, ensuring complete privacy and security.

### How It Works

1. **Upload** — Drag & drop or browse to select a password-protected PDF file.
2. **Authenticate** — Enter the PDF password to unlock the document.
3. **Name & Download** — Choose a custom filename and download the unlocked PDF as `<your_name>_unlocked.pdf`.

Under the hood, the app uses **PDF.js** to decrypt and render each page (supporting RC4, AES-128, and AES-256 encryption), then rebuilds the document as a fresh, unprotected PDF using **jsPDF**.

---

## 🚀 Where It Is Used

| Use Case | Description |
|---|---|
| **Personal Document Access** | Unlock personal PDFs (bank statements, tax forms, insurance documents) where you know the password but want a permanently accessible copy without re-entering credentials every time. |
| **Office & Workplace** | Remove restrictions from internal company documents, reports, or presentations that were shared with a password for transit security but need to be freely accessible once received. |
| **Academic & Research** | Researchers and students can unlock password-protected academic papers, course materials, or institutional documents for easier annotation and reference. |
| **Archival & Backup** | Create unprotected backup copies of important password-protected documents to prevent future lockouts due to forgotten passwords. |
| **Print & Share** | Unlock PDFs that have print/copy restrictions so they can be printed, annotated, or shared within authorized teams. |
| **Privacy-Sensitive Environments** | Organizations handling confidential data (legal, medical, financial) can unlock PDFs without uploading them to third-party online tools, keeping sensitive information offline. |

---

## 🎯 Who Benefits From This App

### 👤 Individual Users
- People who receive password-protected PDFs (bills, receipts, official documents) and want a hassle-free copy for personal records.
- Users who have forgotten the original PDF password but still have access to unlock it one last time.

### 🏢 Business Professionals
- **HR departments** — Unlocking employee documents, contracts, and compliance PDFs shared with temporary passwords.
- **Finance teams** — Accessing password-protected invoices, audit reports, and bank statements.
- **Legal professionals** — Removing encryption from legal filings, contracts, and case documents after review.

### 🎓 Students & Educators
- Students receiving course materials and exam papers as locked PDFs.
- Educators who need to redistribute or annotate protected teaching resources.

### 🔐 Privacy-Conscious Users
- Anyone who refuses to upload sensitive documents to online PDF unlocking services.
- Users in regulated industries (healthcare, banking, government) who cannot use external cloud tools.

### 💻 Developers & IT Teams
- Quick internal tool for dev teams dealing with password-locked config files, documentation, or API specs distributed as PDFs.
- Can be deployed on an internal network as a self-hosted utility — no backend required.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **HTML5** | Page structure and layout |
| **TailwindCSS** (CDN) | Modern, responsive UI styling |
| **PDF.js** v3.11.174 | Decrypts and renders password-protected PDF pages (supports all standard encryption methods) |
| **jsPDF** v2.5.1 | Rebuilds decrypted pages into a new, unlocked PDF document |
| **Inter** (Google Fonts) | Clean, modern typography |

---

## 📂 File Structure

```
index.html    ← Single-file application (no build step, no dependencies to install)
README.md     ← This documentation file
```

---

## ⚡ Quick Start

No installation needed. Simply open the file in any modern browser:

```bash
# Option 1: Double-click index.html in your file explorer

# Option 2: Serve locally (optional)
npx serve .
# Then open http://localhost:3000/index.html
```

### Requirements
- Any modern browser (Chrome, Firefox, Edge, Safari)
- Internet connection on first load (to fetch CDN libraries), works offline after caching

---

## 🔒 Privacy & Security

- **Zero server interaction** — No data leaves your machine. Ever.
- **No file uploads** — The PDF is read directly from your local filesystem via the browser's File API.
- **No tracking or analytics** — The page contains no third-party tracking scripts.
- **Offline capable** — Once the CDN scripts are cached, the tool works completely offline.

---

## ⚠️ Limitations

- **Output is image-based** — The unlocked PDF contains rendered images of each page (not selectable text). This is a trade-off for supporting all encryption types reliably.
- **Large PDFs** — Very large documents (100+ pages) may take longer to process depending on browser memory.
- **User password required** — This tool requires you to know the PDF password. It does not crack or brute-force passwords.

---

## 📜 License

This project is for internal/private use. All processing is self-contained within a single HTML file.
