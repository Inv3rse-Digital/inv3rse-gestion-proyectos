# 🚀 Sistema de Gestión y Portafolio para Inv3rse

## 📋 Resumen Ejecutivo
**Inv3rse** es una empresa dedicada al desarrollo de experiencias creativas inmersivas (AR/VR, Animación 2D/3D y experiencias Phygital). Actualmente, enfrentan una problemática de información dispersa (briefs, presupuestos y feedback en correos), ausencia de un portafolio unificado y un control de versiones nulo en la gestión de proyectos.

Esta solución es un **Sistema Web de Gestión de Proyectos** desarrollado en Java (Spring Boot) que centraliza la operación interna (gestión de clientes, proyectos, estados y avances) y permite a los clientes dar seguimiento en tiempo real al estado de sus entregables.

## 📑 Tabla de Contenidos
1. [Arquitectura de la Solución](#-arquitectura-de-la-solución)
2. [Requerimientos del Sistema](#-requerimientos-del-sistema)
3. [Instalación y Configuración](#-instalación-y-configuración)
4. [Guía de Uso](#-guía-de-uso)
5. [Guía de Contribución](#-guía-de-contribución)
6. [Roadmap a Futuro](#-roadmap-a-futuro)

---

## 🏗️ Arquitectura de la Solución
El sistema sigue una arquitectura en capas (Monolito Modular) separando responsabilidades para facilitar el mantenimiento, alineada con los estándares definidos en la Fase III:
- **Frontend:** Interfaz responsiva desarrollada con HTML5, JavaScript (Fetch API) y Tailwind CSS.
- **Backend:** Spring Boot 3.2.5 con Java 21, manejando la lógica de negocio, controladores REST y persistencia de datos.
- **Capa de Datos:** Base de datos relacional MySQL 8.0 (alojada en la nube vía HostGator) para la integridad de la información.
- **CI/CD:** GitHub Actions configurado para compilar el proyecto y ejecutar pruebas unitarias con JUnit en cada push a las ramas `develop` o `main`.

---

## ⚙️ Requerimientos del Sistema
Para ejecutar este proyecto en un ambiente de desarrollo o producción, se requiere:
- **Lenguaje:** Java JDK 21 (Temurin o superior).
- **Base de Datos:** MySQL 8.0.
- **Herramienta de Build:** Apache Maven 3.9+.
- **IDE Recomendado:** Apache NetBeans o IntelliJ IDEA.
- **Navegador:** Chrome, Edge, Safari o Firefox (últimas 2 versiones).

---

## 🛠️ Instalación y Configuración

### 1. Clonar el repositorio
```bash
git clone https://github.com/TU_USUARIO_GITHUB/inv3rse-gestion-proyectos.git
cd inv3rse-gestion-proyectos
