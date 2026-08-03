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
git clone https://github.com/Inv3rse-Digital/inv3rse-gestion-proyectos.git
cd inv3rse-gestion-proyectos
```

### 2. Configuración del Producto
El archivo principal de configuración es src/main/resources/application.properties. Debes configurar las credenciales de tu base de datos (por seguridad, este archivo está en .gitignore en producción):
```bash
spring.datasource.url=jdbc:mysql://TU_HOST:3306/TU_BASE_DE_DATOS
spring.datasource.username=TU_USUARIO_BD
spring.datasource.password=TU_CONTRASEÑA_BD
spring.jpa.hibernate.ddl-auto=update
server.port=9090
```
### 3. Configuración del Producto
Abre el proyecto en tu IDE.
Ejecuta mvn clean compile para verificar dependencias.
Ejecuta las pruebas unitarias con mvn test (valida el contexto de Spring Boot).
Ejecuta la clase principal GestionProyectosApplication.java.
Accede a http://localhost:9090 en tu navegador.

### 4. Implementación en Producción (Local o Nube)
Para generar el artefacto ejecutable:
```bash
mvn clean package
```
Esto generará un archivo .jar en la carpeta target/. Para ejecutarlo en cualquier servidor (o nube como Railway/Heroku):
```bash
java -jar target/gestion-proyectos-0.0.1-SNAPSHOT.jar
```
### 📖 Guía de Uso 📖 
Referencia para Usuario Final (Cliente)
Acceder a la página principal y seleccionar "Soy Cliente".
Si es nuevo, registrarse llenando el formulario de alta (Nombre, Usuario, Email, Empresa, Contraseña).
Iniciar sesión con las credenciales creadas.
Visualizar el dashboard con el estado del proyecto asignado, fecha estimada de entrega, tipo de proyecto (ej. Realidad Mixta, Animación 3D) y avances visuales cargados por el equipo.
Referencia para Usuario Administrador (Área Creativa)
Acceder a /admin-login.html con las credenciales de administrador (Usuario: admin, Contraseña: inv3rse).
En el tablero tipo Kanban, visualizar todos los proyectos activos.
Hacer clic en una tarjeta para editar: nombre, tipo, fecha de entrega, estado (Planeación, Desarrollo, Entregado) y reasignar el cliente responsable.
Agregar notas de avance en la bitácora y URLs de imágenes de progreso.

### 🤝 Guía de Contribución
Este proyecto sigue el flujo de trabajo establecido en la Fase III. Para contribuir:

1. Clonar el repositorio y ubicarse en la rama de desarrollo:
```bash
git checkout develop
```

2. Crear una nueva rama para la funcionalidad o corrección:
```bash
 git checkout -b feature/nombre-de-la-funcionalidad
```

3. Realizar los cambios, asegurando que las pruebas de JUnit pasen (mvn test), y hacer commit:
```bash
   git commit -m "feat: descripción clara del cambio"
```

4. Subir la rama al repositorio remoto:
```bash
  git push origin feature/nombre-de-la-funcionalidad
```

5. Abrir un Pull Request en GitHub hacia la rama develop.

6. Esperar la revisión de código, la validación del pipeline de GitHub Actions y el merge por parte del mantenedor del proyecto.

### 🗺️ Roadmap a Futuro
Implementación de autenticación robusta con JWT (JSON Web Tokens) y encriptación de contraseñas (BCrypt).
Módulo de carga real de archivos (imágenes/PDFs) integrado con un servicio de almacenamiento en la nube (AWS S3 o Cloudinary).
Sistema de notificaciones automáticas por correo electrónico al cliente cuando el estado del proyecto cambie.
Dashboard administrativo con gráficas de progreso y métricas de rendimiento del equipo.


