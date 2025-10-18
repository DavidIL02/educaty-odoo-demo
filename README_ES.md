# 🎓 Educaty — Demo Odoo 17 (Website → CRM → Ventas → Contabilidad)

**Autor:** [David Josué Ibáñez Leal](https://www.linkedin.com/in/david-josué-ibá%C3%B1ez-leal-b03b25376/)  
**Demo en vivo:** [https://educaty.odoo.flybots.agency/](https://educaty.odoo.flybots.agency/)  
**Stack:** Odoo 17 · Docker · PostgreSQL · Nginx Proxy · TLS (Let's Encrypt)  
**Hosting:** Hetzner Cloud (Ubuntu 24.04)  

---

## 🧭 Contexto

Educaty era originalmente un sitio WordPress básico con trazabilidad limitada y sin integración entre procesos.  
Las solicitudes de los clientes no estaban conectadas con CRM, Ventas ni Contabilidad, lo que generaba trabajo manual y poca visibilidad.

Esta **demo de Odoo 17 Community Edition** muestra cómo solucionar esas brechas mediante un flujo ERP totalmente integrado:

> **Website → CRM → Ventas → Contabilidad**

Todos los módulos están conectados para demostrar cómo una empresa educativa puede digitalizar sus operaciones de extremo a extremo.

---

## ⚙️ Infraestructura

| Capa | Tecnología | Descripción |
|------|-------------|-------------|
| ☁️ Hosting | Hetzner Cloud (Ubuntu) | VPS privado para desarrollo y demo |
| 🐳 Orquestación | Docker Compose | Stack multicontenedor |
| 🌐 Proxy inverso | jwilder/nginx-proxy + Let's Encrypt | Configuración automática de vhosts + certificados TLS |
| 🗄️ Base de datos | PostgreSQL (centralizada) | Compartida entre contenedores Odoo |
| 🧠 ERP | Odoo 17 Community | Arquitectura modular (CRM, Ventas, Contabilidad, Portal) |
| 🧩 Red | Red externa `proxy` | Conexión segura entre servicios detrás del proxy SSL |
| ⚙️ Configuración | `odoo.conf` personalizada | dbfilter, list_db, admin_passwd, wkhtmltopdf, web.base.url |

---

## 💼 Flujo de negocio (E2E)

1. **Formulario web** → crea un **Lead** en CRM  
2. **Lead** → convertido en **Presupuesto de venta**  
3. **Presupuesto** → enviado como **PDF o por email**  
4. **Confirmación del presupuesto** → se convierte en **Pedido de venta**  
5. **Factura** → generada automáticamente en Contabilidad  
6. **Registro de pago** → reflejado en la contabilidad  
7. **Portal del cliente** → descarga del PDF final de factura  

📄 **Módulos instalados:**  
Website · CRM · Ventas · Contabilidad 

---

## 🧠 Aprendizajes técnicos

- Ajuste fino de `dbfilter`, `list_db` y `web.base.url`  
- Restauración de base de datos con soporte de filestore  
- Gestión de certificados TLS y corrección del error `413 Request Entity Too Large`  
- Configuración de `wkhtmltopdf` para generación de PDFs  
- Optimización del stack mínimo de módulos (MVP)  
- Uso de redes Docker para comunicación entre servicios  

---

## 🚀 Próximos pasos

- Añadir módulo de **eCommerce** y **pasarelas de pago** (Stripe / PayPal)  
- Ampliar **Marketing y envíos masivos de correo**  
- Integrar **capa de automatización Flybots (n8n)** con datos Odoo  
- Conectar **asistentes IA (OpenAI API)** para automatizar procesos de ventas  

---

## 👨‍💻 Sobre el autor

**David Josué Ibáñez Leal** — Desarrollador y entusiasta de la automatización
Actualmente construyendo demos reales de ERP y soluciones de automatización usando **Odoo, Docker y n8n**.

🧩 Explorando la intersección entre **DevOps, consultoría ERP y automatización empresarial.**  
☁️ Construyendo un laboratorio personal en **Hetzner Cloud** para aprender y demostrar casos reales de transformación digital.

**Conecta conmigo:**  
🔗 [LinkedIn](https://www.linkedin.com/in/david-josué-ibá%C3%B1ez-leal-b03b25376/)  
💻 [GitHub](https://github.com/DavidIL02)  

---
