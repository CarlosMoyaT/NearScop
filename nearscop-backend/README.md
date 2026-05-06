# 🌍 NearEarth — Dashboard de Asteroides Cercanos

**Proyecto de Portfolio — Junior Developer**
Spring Boot · Angular · Docker · CI/CD · NASA NeoWs API

---

## 🚀 Resumen del Proyecto

NearEarth es una aplicación web fullstack que consume la API pública de NASA (NeoWs) para mostrar asteroides cercanos a la Tierra en un dashboard interactivo.

Incluye:

* Visualización de datos en gráficas
* Sistema de clasificación de peligrosidad (DangerScore)
* Filtros avanzados por fecha y características

🎯 **Objetivo:** demostrar habilidades reales en backend, frontend y DevOps con un stack demandado en el mercado.

---

## 🧠 Diferenciadores del Proyecto

* 🌐 Datos reales (NASA API)
* 🏗️ Arquitectura limpia y explicable
* ⚙️ Stack profesional (Spring Boot + Angular)
* 🚀 Deploy accesible online
* 📄 Documentación técnica cuidada

---

## 🛠️ Stack Tecnológico

### Backend

* Java 21
* Spring Boot 3
* WebClient (API calls)
* Caffeine Cache (TTL)
* Spring Validation
* Swagger (OpenAPI)
* JUnit 5 + Mockito
* Maven

### Frontend

* Angular 17 (Standalone Components)
* TypeScript (strict mode)
* RxJS + Signals
* Angular Material
* Chart.js / ApexCharts

### DevOps

* Docker + Docker Compose
* GitHub Actions (CI/CD)
* Deploy:

    * Backend: Render / Railway
    * Frontend: Vercel / Netlify

---

## 🏗️ Arquitectura

### Backend — Layered Architecture

* **Controller**

    * Maneja requests HTTP
* **Service**

    * Lógica de negocio
* **Client**

    * Comunicación con NASA API
* **DTO / Model**

    * Separación de datos internos y externos

### Flujo de datos

1. Frontend solicita datos (`/asteroids`)
2. Controller valida request
3. Service consulta caché
4. Si no hay datos → Client llama a NASA API
5. Se transforman datos y se calcula `DangerScore`
6. Respuesta al frontend

---

## 📂 Estructura del Proyecto

### Backend

```
nearearth-backend/
├── controller/
├── service/
├── client/
├── dto/
├── model/
├── config/
└── test/
```

### Frontend

```
nearearth-frontend/
├── core/
├── features/
├── shared/
└── environments/
```

---

## 🔌 API REST

**Base URL:** `/api/v1`

### Endpoints

* `GET /asteroids` → lista por rango de fechas
* `GET /asteroids/{id}` → detalle
* `GET /asteroids/today` → hoy
* `GET /asteroids/stats` → estadísticas
* `GET /health` → estado del servicio

---

## ⭐ Feature Clave: DangerScore

Sistema propio que calcula la peligrosidad del asteroide (0–100) basado en:

* Velocidad
* Distancia
* Tamaño

👉 Esto demuestra lógica de negocio real (no solo consumo de API).

---

## 🗺️ Roadmap

* [ ] Fase 1: Setup + conexión NASA API
* [ ] Fase 2: Caché + manejo de errores
* [ ] Fase 3: Frontend básico
* [ ] Fase 4: Gráficas
* [ ] Fase 5: Docker
* [ ] Fase 6: CI/CD + deploy

---

## 🧪 Testing Strategy

* Unit tests (Service + lógica)
* Controller tests (`@WebMvcTest`)
* Integration tests (`@SpringBootTest`)
* Mocking con Mockito

---

## ⚙️ CI/CD

GitHub Actions:

* Build backend
* Tests
* Build frontend
* Docker image

---

## 🐳 Docker

```bash
docker-compose up
```

Levanta:

* Backend (Spring Boot)
* Frontend (Angular)

---

## 📄 Cómo Ejecutar el Proyecto

```bash
git clone <repo>
cd nearearth
docker-compose up
```

---

## 🎤 Pitch para Entrevista

> NearEarth es un dashboard que consume la API de NASA para mostrar asteroides cercanos. Implementé un algoritmo propio llamado DangerScore que calcula la peligrosidad combinando múltiples variables. El proyecto demuestra arquitectura limpia, testing y despliegue completo con Docker y CI/CD.

---

## 📌 Mejoras Futuras

* Base de datos (histórico)
* Autenticación JWT
* Alertas en tiempo real
* Sistema de usuarios

---

## ✅ Checklist Final

* [ ] Repo en GitHub
* [ ] README completo
* [ ] Demo online
* [ ] CI funcionando
* [ ] Docker funcional

---

**NearEarth — Portfolio Project**
