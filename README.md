# Educaty Odoo Demo

## Context
I am **David Josué Ibáñez Leal**. This is a personal challenge: deploying an Odoo 17 instance in **one week** with no prior Odoo experience, running on Hetzner (Docker, Nginx, PostgreSQL, reverse proxy + TLS).

## Infrastructure
- Hetzner Cloud (Ubuntu)
- Docker Compose orchestration
- jwilder/nginx-proxy + letsencrypt companion (TLS)
- PostgreSQL (central)
- Odoo 17 application
- vhost override: client_max_body_size 256m
- External Docker network: proxy

## Business Flow (E2E)
Website form  CRM lead  Sales quotation (PDF/email)  Confirm to Sales Order  Accounting invoice  Register payment  final PDF.

## Lessons Learned
- dbfilter, list_db, web.base.url in odoo.conf
- Restore DB with filestore
- wkhtmltopdf, TLS renewal, 413 body size fix
- Minimal MVP modules: Website, CRM, Sales, Accounting, Portal, l10n_es

## Author
**David Josué Ibáñez Leal** — [GitHub](https://github.com/DavidIL02)
