# Diseño Maestro | Portafolio Digital de Sebas

Sitio web y portafolio interactivo de **Diseño Maestro**, desarrollado para **Sebas** (Ilustrador, diseñador de personajes y escenarios). El diseño sigue una estética de alto contraste (Dark Mode con acentos en verde esmeralda y neón), pensada para *"mentes hiperactivas"*.

---

## 🚀 Cómo Visualizar el Proyecto

Puedes abrir y probar el proyecto de dos formas:

### Opción 1: Apertura Directa en el Navegador
1. Dirígete a la carpeta:
   `C:\Users\57313\.gemini\antigravity\scratch\diseno-maestro`
2. Haz doble clic en cualquiera de los archivos HTML:
   - `index.html` (Página de Inicio con slider interactivo y muestra simétrica)
   - `trabajos.html` (Portafolio de proyectos en cuadrícula Masonry con vista de etapas del proceso)
   - `acerca-de-mi.html` (Historia editorial de Sebas y filosofía de marca)

### Opción 2: Servidor Local Rápido (Recomendado)
Abre una terminal PowerShell o CMD en la carpeta del proyecto y ejecuta:
```bash
python -m http.server 8000
```
Luego abre tu navegador en [http://localhost:8000](http://localhost:8000).

---

## 📂 Estructura de Archivos

```
diseno-maestro/
│
├── index.html                  # Página 1: Inicio (Slider interactivo, propuesta de valor y servicios)
├── trabajos.html               # Página 2: Trabajos (Galería Masonry asimétrica y filtros)
├── acerca-de-mi.html           # Página 3: Acerca de Mí (Historia editorial de Sebas y visión de marca)
│
├── css/
│   ├── style.css               # Variables del sistema de diseño (colores, tipografía Space Grotesk/Inter, botones, badges)
│   ├── header-footer.css       # Header de 2 bloques (Nav y Banner dinámico) y Footer de 3 columnas (Contacto, Redes y Mapa)
│   ├── animations.css          # Transición de opacidad escalonada, barrido "slash" de izq. a der., hover y pulso neón
│   ├── modal.css               # Ventana modal interactiva "El Trayecto de la Composición" (Boceto -> Lineart -> Color -> Render)
│   └── pages.css               # Estilos de secciones de Inicio, Grid Masonry y diseño editorial de Acerca de Mí
│
├── js/
│   ├── projects-data.js        # Mock data detallado con imágenes, desafíos narrativos y las 4 etapas del trayecto
│   ├── slider.js               # Carrusel interactivo para Header Bloque 2 en Inicio (autoplay, hover pause, swipe, dots)
│   ├── gallery.js              # Controlador de la galería asimétrica en Trabajos (filtros, hover y apertura de modal)
│   ├── modal.js                # Lógica del modal con selector de etapas 1 a 4 y enlace directo a WhatsApp
│   └── main.js                 # Navegación móvil (hamburguesa), página activa e IntersectionObserver para animaciones
│
└── assets/                     # Directorio para futuros recursos locales (iconos, imágenes webp y renders)
```

---

## 🎨 Sistema de Diseño Implementado

* **Fondo Principal:** `#0D0D0D` (Negro profundo con alto contraste)
* **Superficies y Tarjetas:** `#141416` / `#18181C` (Gris carbón)
* **Color Primario (Acento):** `#10B981` / `#22C55E` (Verde esmeralda y verde vibrante con resplandor neón)
* **Tipografía:** *Space Grotesk* para titulares con impacto visual + *Inter* para máxima legibilidad en párrafos.
* **Componentes Globales:**
  * **Header:** Bloque 1 (Navegación + Logo interactivo + Menú móvil) y Bloque 2 (Banner dinámico específico por vista).
  * **Footer:** Columna 1 (Contacto con enlaces `tel:` y `mailto:`), Columna 2 (WhatsApp destacado y redes sociales) y Columna 3 (Google Maps interactivo).
* **Interacciones Clave:**
  * Animación de **opacidad suave escalonada (0 a 1)** al hacer scroll en la cuadrícula simétrica de Inicio.
  * Efecto **Slash / Barrido de izquierda a derecha** en la ilustración de servicios.
  * Visualizador interactivo del **"Trayecto de la Composición"**: permite alternar entre Boceto inicial, Lineart, Color base y Render final con notas técnicas explicativas.
