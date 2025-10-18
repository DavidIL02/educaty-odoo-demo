# 🎓 Educaty — Odoo 17 Demo (Website → CRM → Sales → Accounting)

**Author:** [David Josué Ibáñez Leal](https://www.linkedin.com/in/david-josué-ibá%C3%B1ez-leal-b03b25376/)  
**Live Demo:** [https://educaty.odoo.flybots.agency/](https://educaty.odoo.flybots.agency/)  
**Stack:** Odoo 17 · Docker · PostgreSQL · Nginx Proxy · TLS (Let's Encrypt)  
**Hosting:** Hetzner Cloud (Ubuntu 24.04)  

---

## 🧭 Context

Educaty originally had a basic WordPress site with limited traceability and no process integration.  
Customer requests weren’t connected to CRM, Sales, or Accounting, resulting in manual work and lack of visibility.

This **Odoo 17 Community Edition demo** shows how those gaps can be solved with a unified ERP flow:

> **Website → CRM → Sales → Accounting**

All modules are integrated to demonstrate how an educational service business could digitalize its operations end-to-end.

---

## ⚙️ Infrastructure Overview

| Layer | Technology | Description |
|-------|-------------|-------------|
| ☁️ Hosting | Hetzner Cloud (Ubuntu) | Private VPS for development and demo |
| 🐳 Orchestration | Docker Compose | Multi-container stack |
| 🌐 Reverse Proxy | jwilder/nginx-proxy + Let's Encrypt | Automatic vhost + TLS |
| 🗄️ Database | PostgreSQL (centralized) | Shared between Odoo containers |
| 🧠 ERP | Odoo 17 Community | Modular architecture (CRM, Sales, Accounting, Portal) |
| 🧩 Networking | External `proxy` network | Linked containers behind SSL proxy |
| ⚙️ Config | Custom `odoo.conf` | dbfilter, list_db, admin_passwd, wkhtmltopdf path |

---

## 💼 Business Flow (E2E)

1. **Website Form** → creates a **Lead** in CRM  
2. **Lead** → converted into a **Sales Quotation**  
3. **Quotation** → sent as **PDF or Email**  
4. **Quotation Confirmation** → becomes **Sales Order**  
5. **Invoice** → automatically generated in Accounting  
6. **Payment Registration** → reflected in Accounting  
7. **Customer Portal** → downloadable final PDF invoice  

📄 **Modules installed:**  
Website · CRM · Sales · Accounting   

---

## 🧠 Technical Learnings

- Fine-tuned `dbfilter`, `list_db`, and `web.base.url`  
- Database restore with filestore support  
- Handled TLS renewals and `413 Request Entity Too Large` issue  
- Configured `wkhtmltopdf` for PDF generation  
- Optimized minimal MVP module stack  
- Used Docker networks for cross-service communication  

---

## 🚀 Future Plans

- Add **eCommerce** and **payment gateways** (Stripe / PayPal)  
- Extend **Marketing & Mass Mailing** modules  
- Deploy **Flybots automation layer (n8n)** for Odoo data workflows  
- Integrate **AI assistants** via OpenAI API for sales automation  

---

## 👨‍💻 About the Author

**David Josué Ibáñez Leal** — Developer & Automation Enthusiast 🇪🇸🇨🇴  
Currently building real-world ERP demos and automation solutions using **Odoo, Docker, and n8n**.

🧩 Exploring the intersection between **DevOps, ERP consulting, and business automation.**  
☁️ Building a personal lab on **Hetzner Cloud** to learn and showcase end-to-end digital transformation use cases.

**Connect:**  
🔗 [LinkedIn](https://www.linkedin.com/in/david-josué-ibá%C3%B1ez-leal-b03b25376/)  
💻 [GitHub](https://github.com/DavidIL02)  

