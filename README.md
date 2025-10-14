# 🧩 Educaty Odoo Demo

## 🧭 Context

**Educaty** originally had a simple **WordPress site** with very limited traceability and poor process integration.  
Customer requests were not connected to CRM, Sales, or Accounting — leading to inefficiency and manual work.  

This **Odoo 17 demo** shows how those gaps can be solved with an integrated flow:  
**Website → CRM → Sales → Accounting**, all connected within one unified platform.

---

## ⚙️ Infrastructure

- ☁️ Hetzner Cloud (Ubuntu)
- 🐳 Docker Compose orchestration
- 🌐 jwilder/nginx-proxy + Let's Encrypt companion (TLS)
- 🗄️ Centralized PostgreSQL database
- 🧠 Odoo 17 Community Edition
- ⚙️ vhost override: `client_max_body_size 256m`
- 🔗 External Docker network: `proxy`

---

## 💼 Business Flow (E2E)

1. **Website Form** → Lead is created in CRM  
2. **CRM Lead** → Converted into Sales Quotation  
3. **Sales Quotation** → Sent as PDF or Email  
4. **Quotation Confirmation** → Becomes Sales Order  
5. **Accounting Invoice** → Generated automatically  
6. **Payment Registration** → Recorded in Accounting  
7. **Final PDF** → Downloadable by the customer through the Portal  

---

## 🧠 Lessons Learned

- Fine-tuning of `dbfilter`, `list_db`, and `web.base.url` in `odoo.conf`  
- Database restore with **filestore**  
- Handling **wkhtmltopdf**, TLS renewal, and 413 “Request Entity Too Large” fix  
- Minimal MVP modules: `Website`, `CRM`, `Sales`, `Accounting`, `Portal`, `l10n_es`

---

## 👨‍💻 Author

**David Josué Ibáñez Leal**  
Personal DevOps & Automation Lab — exploring ERP integration and business automation with Odoo.

💼 [LinkedIn — David Josué Ibáñez Leal](https://www.linkedin.com/in/david-josu%C3%A9-ib%C3%A1%C3%B1ez-leal-b03b25376/)
