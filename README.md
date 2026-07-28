# 🚀 Sistema de Gestión y Portafolio para Inv3rse

## 📋 Resumen Ejecutivo
**Inv3rse** es una empresa mexicana dedicada al desarrollo de experiencias creativas inmersivas (AR/VR). Actualmente, enfrentan una problemática de información dispersa (briefs, presupuestos y feedback en correos y Excels), ausencia de un portafolio unificado y control de versiones nulo. 

Esta solución es un **Sistema Web de Gestión y Portafolio** desarrollado en Java (Spring Boot) que centraliza la operación interna (gestión de clientes, proyectos y multimedia) y expone el trabajo de la empresa al exterior mediante un portafolio público interactivo.

## 📑 Tabla de Contenidos
1. [Arquitectura de la Solución](#-arquitectura-de-la-solución)
2. [Requerimientos del Sistema](#-requerimientos-del-sistema)
3. [Instalación y Configuración](#-instalación-y-configuración)
4. [Guía de Uso](#-guía-de-uso)
5. [Guía de Contribución](#-guía-de-contribución)
6. [Roadmap a Futuro](#-roadmap-a-futuro)

---

## 🏗️ Arquitectura de la Solución
El sistema sigue una arquitectura de microservicios (o monolito modular) separando responsabilidades para facilitar el mantenimiento:
- **Frontend**: Interfaz responsiva (Mobile-first) con HTML5, CSS3 y Bootstrap 5.
- **Backend**: Spring Boot 4.1.0 con Java 21, manejando la lógica de negocio, autenticación JWT y gestión de archivos.
- **Capa de Datos**: MySQL 8.0 para la integridad de datos relacionales y almacenamiento local en servidor para assets multimedia pesados.
- **CI/CD**: GitHub Actions para compilación y ejecución automática de pruebas JUnit en cada push.

---

## ⚙️ Requerimientos del Sistema
Para ejecutar este proyecto en un ambiente de desarrollo o producción, se requiere:
- **Java**: JDK 21 (Temurin o superior).
- **Base de Datos**: MySQL 8.0.
- **Herramienta de Build**: Apache Maven 3.9+.
- **Sistema Operativo**: Windows, macOS o Linux.
- **Navegador**: Chrome, Edge, Safari o Firefox (últimas 2 versiones).

---

## 🛠️ Instalación y Configuración

### 1. Clonar el repositorio
```bash
git clone https://github.com/inv3rse-digital/inv3rse-gestion-proyectos.git
cd inv3rse-gestion-proyectos
