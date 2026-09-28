---
name: google-dev-engineering
description: Estándares oficiales de Ingeniería y Desarrollo en Google Cloud Platform (GCP) para la Biblioteca Virtual BEP. Incluye arquitectura Cloud Run + Directus + Cloud SQL + GCS, RBAC con JWT/Cookies HttpOnly, Signed URLs DLP (15 min), validación Zod, cabeceras de seguridad HTTP, Vitest/Supertest/Playwright y Google Cloud Logging en formato JSON.
---

# Google Cloud Platform (GCP) Engineering & Software Development Skill

Esta skill encapsula los estándares técnicos oficiales del **Google Cloud Architecture Framework** y las guías de ingeniería para la **Biblioteca Virtual BEP (Breca Executive Program)**.

---

## 1. Arquitectura Tecnológica en GCP
- **Frontend Web (Cloud Run):** Despliegue en contenedor Docker stateless (React/Next.js). Autoescalado desde 0, renderizado ultra rápido y protección de rutas.
- **Panel Admin CMS (Cloud Run):** Directus Headless CMS para autogestión de plantillas de sesiones, versionado de documentos y carga asíncrona (*direct-to-storage*).
- **Base de Datos Relacional (Cloud SQL):** PostgreSQL v15+ para metadatos estructurados, historial de interacción y permisos.
- **Almacenamiento Binario (Cloud Storage GCS):** Buckets privados para videos HD (streaming HTTP Range 206), PPTX, PDFs y galerías de fotos.
- **Identity & Access Control:** Integration con Identity-Aware Proxy (IAP) y Auth.js para verificación de identidad corporativa Grupo Breca.

---

## 2. Capa de Seguridad y Estándares Técnicos
1. **RBAC & Cookies Seguras:**
   - Separación estricta entre `ROLE_LIDER` (Visualizador de catálogo, favoritos, lecturas in-app) y `ROLE_ADMIN` (Editor, analítica, carga de recursos).
   - Cookies autenticadas con banderas `HttpOnly`, `Secure` y `SameSite=Strict`.
2. **DLP & Signed URLs (Control de Fugas de Información):**
   - Cero acceso público a objetos GCS.
   - Acceso a streaming y descargas mediante **Signed URLs con expiración corta (máximo 15 minutos)** generadas dinámicamente desde la API Backend.
3. **Sanitización de Entradas (Zod Validation):**
   - Esquemas **Zod** obligatorios en API Routes para validar y sanitizar payloads JSON, eliminando vectores XSS e inyecciones SQL/NoSQL.
4. **Cabeceras HTTP Seguras:**
   - `Content-Security-Policy` (CSP) estricta.
   - `Strict-Transport-Security` (HSTS).
   - `X-Content-Type-Options: nosniff`.
   - `X-Frame-Options: SAMEORIGIN`.
   - `Referrer-Policy: strict-origin-when-cross-origin`.

---

## 3. Testing, Debugging y Observabilidad en GCP
- **Pruebas Unitarias e Integración (Vitest + Supertest):** Cobertura de lógica de negocio y endpoints API. Verificación estricta de rechazo a perfiles no autorizados (`GUEST`).
- **Pruebas End-to-End (Playwright):** Cobertura del flujo crítico: Login corporativo, filtrado de sesiones en < 2 clics, previsualización in-app de PDF/Video y descarga segura con Signed URL.
- **Google Cloud Logging Structurado:** Logs emitidos en formato JSON legible por GCP Log Explorer (`severity`, `timestamp`, `message`, `httpRequest`, `labels`).
- **Strict TypeScript:** `tsconfig.json` con `"strict": true` activado obligatoriamente en backend y frontend.
