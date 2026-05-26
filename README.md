# 🐕 DogCare Backend - Gestión de Guardería & Residencia Canina

[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2+-6DB33F?logo=spring&logoColor=white)](https://spring.io/projects/spring-boot)
[![Java](https://img.shields.io/badge/Java-17+-007396?logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![Architecture](https://img.shields.io/badge/Architecture-Hexagonal-orange)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()

Aplicación backend para la gestión integral de una **guardería, residencia y servicio de paseos caninos**. 
Proyecto diseñado **paso a paso como tutorial didáctico** para aprender desarrollo web profesional con Spring Boot 3, arquitectura hexagonal y buenas prácticas de ingeniería de software.

---

## 📖 ¿Qué hace esta app?
- 📝 Registro de dueños y mascotas con datos detallados (alimentación, paseos, costumbres, sociabilidad).
- 📅 Gestión de reservas por tipo de servicio: guardería, residencia, paseo o mixto.
- 👥 Asignación de trabajadores (cuidadores/paseadores) y control de ocupación diaria.
- 💰 Cálculo automático de precios, check-in/check-out y historial por mascota.
- 🔐 Control de acceso por roles: Administrador, Trabajador y Cliente.

---

## 🛠️ Stack Tecnológico
| Capa | Tecnología |
|------|------------|
| **Backend** | Spring Boot 3.x, Java 17, Maven, Lombok, Jakarta Validation |
| **Arquitectura** | Hexagonal (Ports & Adapters) |
| **Base de Datos** | MySQL 8.0, Spring Data JPA |
| **Documentación** | SpringDoc OpenAPI (Swagger UI) |
| **Frontend** (Fase futura) | React 18 + Vite + TypeScript + Tailwind/MUI |
| **DevOps** | Docker & Docker Compose |

---

## 🏗️ Arquitectura Hexagonal
Este proyecto sigue el patrón **Ports & Adapters**:
- 🔵 **Dominio (`domain/`)**: Lógica de negocio pura. Sin dependencias de Spring, JPA o HTTP.
- 🟡 **Aplicación (`application/`)**: Casos de uso que orquestan reglas y transacciones.
- 🟢 **Adaptadores (`adapter/`)**: Puentes con el exterior (REST API, MySQL, validadores, mappers).

✅ **Ventaja didáctica**: Puedes testear la lógica de negocio sin levantar Spring ni una base de datos. Cambiar de MySQL a PostgreSQL o añadir una API móvil solo implica crear nuevos adaptadores.

---

## 📚 Estructura del Tutorial
El proyecto está dividido en fases progresivas. Cada una incluye código, explicación y notas para grabación/documentación:

| Fase | Contenido | Estado |
|------|-----------|--------|
| `01` | 📐 Análisis, UML y casos de uso | ✅ Completado |
| `02` | 🗃️ Diseño de base de datos y script SQL | ✅ Completado |
| `03` | ⚙️ Setup Spring Boot + Docker + estructura hexagonal | ✅ Completado |
| `04` | 🧱 Dominio puro, puertos y adaptadores JPA | 🔄 En progreso |
| `05` | 🔐 Spring Security + JWT + roles | ⏳ Pendiente |
| `06` | 📅 Lógica de reservas, validaciones y asignaciones | ⏳ Pendiente |
| `07` | ⚛️ Frontend React + consumo de API | ⏳ Pendiente |
| `08` | 🚀 Docker Compose + despliegue + documentación final | ⏳ Pendiente |

---

## ✅ Requisitos Previos
- ☕ Java 17 o superior
- 📦 Maven 3.8+ (incluido `mvnw`)
- 🐳 Docker & Docker Compose (recomendado para MySQL)
- 💻 IDE: IntelliJ IDEA, VS Code o Eclipse
- 🌐 Navegador moderno (para Swagger y futuro frontend)

---

## 🚀 Inicio Rápido

### 1. Clonar y preparar
```bash
git clone https://github.com/TU_USUARIO/dogcare-backend.git
cd dogcare-backend
