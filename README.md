#  Nexus Digital Landing Page Web Full-Stack y API REST con PHP

> Proyecto desarrollado como entrega académica, estructurado bajo un enfoque **Full-Stack** que separa la presentación (Frontend) de la lógica del servidor (Backend).
>
> La aplicación simula una **Landing Page Nexus Digital** para una empresa de desarrollo de software (Nexus Digital) que consume datos de una **API REST en PHP** para cargar secciones dinámicas como "Nosotros" y "Servicios".

---

##  Habilidades Clave Demostradas

###  Programación Front-End (HTML, CSS, JavaScript)

* **Diseño Responsivo (Mobile-First):** Implementación de Media Queries para adaptar el diseño a móviles, tablets y escritorio.
* **Interactividad con JavaScript:** Gestión de la navegación móvil (menú hamburguesa) y funcionalidad de **Modo Oscuro** con persistencia local (`localStorage`).
* **Formularios y Validación:** Formulario de contacto con validaciones de patrón (regex) en HTML5, y envío simulado de datos mediante **`fetch` (AJAX)** a un script PHP.
* **Estilo y Frameworks:** Uso de **Bootstrap 5** para elementos como el carrusel y CSS modular para la apariencia general.

### ⚙️ Programación Back-End (PHP y API REST)

* **Arquitectura Modular:** Separación clara entre `/frontend` y `/backend`, con una subcarpeta `/backend/v1` para la organización de *endpoints* (API).
* **API REST Simulada:** Creación de *endpoints* en PHP (`/services`, `/about-us`, `/mantenedor`) que devuelven respuestas en formato JSON.
* **Seguridad y Conexión:**
    * Implementación de un sistema básico de **Autenticación con Token (Bearer: ciisa)** en los *endpoints* de la API.
    * Simulación de conexión a base de datos (`conexion.php`) y la estructura SQL (DDL y CRUD) necesaria (`query.sql`).
* **Manejo de Solicitudes:** El script `contacto.php` está configurado para recibir y procesar datos enviados por el método POST, limpiando las entradas con `htmlspecialchars`.

###  Integración (Consumo de API)

* **Uso de `fetch`:** El Front-End utiliza JavaScript para realizar peticiones **`GET`** a las rutas simuladas de la API.
* **Datos Dinámicos:** Las secciones "Nosotros" y "Servicios" se construyen dinámicamente inyectando HTML en el DOM con datos obtenidos desde la API.

---

##  Tecnologías Utilizadas

* **Frontend:** HTML5, CSS3, JavaScript, Bootstrap 5.
* **Backend:** PHP, MySQL (simulado en SQL).
* **Arquitectura:** API REST, Full-Stack modular.

---

#  Ejecución y Despliegue

Este proyecto tiene dos métodos principales de ejecución: una versión estática de la *Landing Page* (desplegada en GitHub Pages) y una versión completa que requiere un servidor local para procesar el *backend* PHP.

---

## Ejecución en Línea (Versión Estática)

La **Landing Page principal** es completamente estática (construida con HTML, CSS y JavaScript) y puede verse de inmediato sin necesidad de un servidor.

* **Despliegue con GitHub Pages:**
    Esta versión está publicada profesionalmente mediante el servicio gratuito GitHub Pages

* **Ver el Resultado Final:**
    Haga clic en el siguiente botón para acceder directamente al sitio web en línea:

    [![Ver Sitio Web](https://img.shields.io/badge/Ver%20Sitio%20Web-2A65F6?style=for-the-badge&logo=materialdesign&logoColor=white)](https://ejts29.github.io/Nexus-Digital-LandingPageWeb-FullStack-PHP-API-REST/)

---

## Ejecución Local (Versión Full Stack con PHP)

El proyecto incluye un ***backend* y una API REST desarrollada en PHP** que requiere un entorno de servidor local para su procesamiento.

Para ejecutar la aplicación en su totalidad (incluyendo la funcionalidad del lado del servidor PHP), siga estos pasos:

1.  **Requisitos:** Debe tener instalado un entorno de servidor local que pueda procesar PHP, como **XAMPP** o **WAMP**.

2.  **Montar el Servidor:**
    * Coloque la carpeta raíz del proyecto, **`Nexus-Digital-LandingPageWeb-FullStack-PHP-API-REST`**, dentro del directorio de documentos de su servidor (típicamente llamado `htdocs` en XAMPP o `www` en WAMP).

3.  **Acceso Local:**
    * Acceda a la *Landing Page* a través de la siguiente URL en su navegador:
        `http://localhost/Nexus-Digital-LandingPageWeb-FullStack-PHP-API-REST/frontend/index.html`

    * Desde esta ubicación, el *frontend* podrá comunicarse con los archivos PHP del *backend*.

##  Estructura del Proyecto

El proyecto sigue una arquitectura modular y separada

```
.
├── backend/                       # Servidor y Lógica de la API (PHP)
│   ├── v1/                        # Versión 1.0 de la API
│   │   ├── about-us/              # Endpoint de 'Nosotros'
│   │   ├── mantenedor/            # Endpoint de Mantenedor (CRUD simulado)
│   │   └── services/              # Endpoint de 'Servicios'
│   │   ├── conexion.php           # Simulación de conexión a DB (clase)
│   │   ├── query.sql              # Estructura de la Base de Datos (DDL/DML)
│   │   └── version1.php           # Configuración y Tokens de la API
│   └── index.php                  # Script raíz del Backend
├── frontend/                      # Interfaz de Usuario (HTML, CSS, JS)
│   ├── assets/
│   │   ├── iconos/
│   │   └── imagenes/
│   ├── css/
│   │   └── styles.css
│   ├── js/
│   │   └── script.js              # Lógica Front-End y Consumo de API
│   ├── contacto.php               # Script de Formulario (POST handler)
│   └── index.html                 # Página principal
├── documentación del Proyecto.pdf # Documentación Académica
└── README.md
```
DESARROLLO BACKEND v1


