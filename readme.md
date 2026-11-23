# MicroHobby Magazine Navigation Toolbar 🕹️🌐

Una barra de herramientas personalizada (*Toolbar*) clásica para **Mozilla Firefox**, diseñada para facilitar la navegación, consulta y búsqueda entre los números de la mítica revista española de informática y videojuegos **MicroHobby** (ZX Spectrum).

## 📅 Compatibilidad y Contexto Histórico

Desarrollada en **marzo de 2011** utilizando la arquitectura clásica de extensiones de Mozilla (**XUL** / **XPCOM** y manifiesto `install.rdf`), sus especificaciones técnicas son las siguientes:

* **Versiones de Firefox soportadas:** **Firefox 3.6 a Firefox 4.0** (Firefox 4.0 se lanzó oficialmente en marzo de 2011).
* **Arquitectura:** Legacy XUL Overlay (`chrome.manifest`, `.xul`, `.dtd`, `.js`).
* **Nota sobre navegadores actuales:** Esta extensión **no es compatible** con las versiones modernas de Firefox (Firefox 57 Quantum en adelante, que migró exclusivamente al estándar *WebExtensions*).
* **¿Cómo probarla hoy en día?** Para ejecutarla en sistemas actuales, se recomienda utilizar navegadores derivados de Firefox que conservan el soporte para extensiones XUL clásicas, como **Pale Moon** o **Basilisk**, o bien mediante una máquina virtual con **Firefox 3.6 / 4.0**.

## ✨ Características Principales

A partir de la estructura interna del paquete (`.xpi`), la extensión ofrece:

* **Barra de herramientas dedicada (`mhtoolbar.xul`):** Integración directa en la interfaz superior del navegador con gráficos personalizados de la revista (`microhobby.jpg`, `mh001.jpg`, `mh217.jpg` —abarcando desde el primer hasta el último número publicado—).
* **Navegación rápida por ejemplares:** Botones dedicados para moverse cómodamente entre los distintos números (*Primero, Anterior, Siguiente, Último* mediante los iconos `icon_*_record.gif`).
* **Búsqueda avanzada (`adv.js`):** Herramienta integrada para localizar rápidamente contenidos, artículos, programas o números concretos.
* **Soporte Multi-idioma:** Localización nativa integrada tanto en **Español (`es-ES`)** como en **Inglés (`en-US`)**.
* **Panel de Opciones y Acerca de:** Ventanas de configuración personalizada (`mhtopt.xul`) e información de la versión (`about.xul`), respaldadas por preferencias predeterminadas (`defaults.js`).

## 📂 Estructura del Proyecto

```text
├── chrome.manifest              # Registro de paquetes XUL, skins y locales
├── install.rdf                  # Metadatos de instalación y versiones de Firefox
├── whatsnew.txt                 # Registro de cambios y novedades (v0.21)
├── defaults/
│   └── preferences/
│       └── defaults.js          # Preferencias predeterminadas de la extensión
└── chrome/
    ├── content/                 # Lógica y estructura de la interfaz
    │   ├── mhtoolbar.xul        # Interfaz principal de la barra de herramientas
    │   ├── mhtoolbar.js         # Controlador principal y eventos
    │   ├── adv.js               # Lógica de búsqueda avanzada
    │   ├── mhtopt.xul           # Ventana de opciones y configuración
    │   └── about.xul            # Ventana "Acerca de"
    ├── locale/                  # Archivos de traducción (.dtd)
    │   ├── en-US/
    │   └── es-ES/
    └── skin/                    # Hojas de estilo (mhtoolbar.css) e iconos
```

## 🚀 Instalación (Entornos Legacy / Pale Moon)

1. Descarga el archivo `microhobby_magazine_navigation_toolbar-0.21-fx.xpi` desde la sección de *Releases* del repositorio (o comprime el contenido de la raíz en un `.zip` y cámbiale la extensión a `.xpi`).
2. Abre tu navegador compatible (por ejemplo, **Pale Moon** o **Firefox 4.0**).
3. Arrastra el archivo `.xpi` directamente dentro de la ventana del navegador, o dirígete a **Herramientas > Complementos > Instalar complemento desde archivo...**.
4. Reinicia el navegador cuando se te solicite para activar la barra de herramientas.

## 📄 Licencia

Proyecto preservado con fines históricos y de archivo para la comunidad retro de ZX Spectrum y MicroHobby.