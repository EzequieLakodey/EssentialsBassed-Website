# 🛒 BoombleGoom — Essentials Based Website

Un marketplace web global donde las personas pueden comprar y vender productos
físicos, servicios y productos digitales por internet, sin depender de un local
físico. Este repositorio contiene la **base del sitio**: maquetado, estilos y
navegación entre secciones.

> Proyecto nacido como entrega del curso de Desarrollo Web (CoderHouse):
> HTML semántico, SCSS modular, Bootstrap y animaciones al scroll.

---

## ✨ ¿Qué hace?

- **Página de inicio** con banner, carrusel de imágenes, presentación del
  mercado y un mapa de contacto embebido.
- **Catálogo de productos** con galería de tarjetas.
- **Alta de cuenta** (signup) e **inicio de sesión** (login).
- **Sección de servicios** ofrecidos por la comunidad.
- **Formulario de contacto** (asunto, nombre, empresa y e-mail) y footer con
  redes sociales y datos de soporte.
- Diseño **responsive** y animaciones on-scroll con AOS.

---

## 🧱 Stack técnico

| Tecnología | Uso |
|---|---|
| HTML5 | Maquetado semántico de las 5 páginas |
| SCSS ( Sass ) | Hojas de estilo modulares, parciales por componente |
| Bootstrap 5.2.2 | Grid, utilidades y componentes (vía CDN) |
| AOS ( Animate On Scroll ) | Animaciones al hacer scroll (vía CDN) |
| Google Maps Embed | Mapa de contacto |

No hay backend ni build step: el navegador lee `index.html` directo.

---

## 📁 Estructura

```
EssentialsBassed-Website/
├── index.html              # Página de inicio
├── pages/
│   ├── products.html       # Catálogo de productos
│   ├── services.html       # Servicios de la comunidad
│   ├── login.html          # Inicio de sesión
│   ├── signup.html         # Registro de cuenta
│   └── chart.html          # Carrito
├── scss/                   # Fuentes SCSS (modulares)
│   ├── style.scss          # Punto de entrada: importa todos los parciales
│   ├── base/               # variables, mixins, extends, reset
│   └── components/         # header, footer, grid, y estilos por página
├── css/
│   └── style.css           # CSS compilado (el que usa el HTML)
├── assets/                 # Imágenes, íconos SVG y favicon
└── package.json            # Metadatos del proyecto (sin dependencias reales)
```

---

## 🚀 Clonar y preparar

Requisitos: **git** y un navegador. Nada más.

```bash
# 1. Clonar
git clone https://github.com/EzequieLakodey/EssentialsBassed-Website.git
cd EssentialsBassed-Website
```

### Opción A — Abrir directo (lo más simple)

El sitio es 100% estático: abrí `index.html` en el navegador y listo.

```bash
# Linux
xdg-open index.html

# macOS
open index.html
```

### Opción B — Con servidor local (recomendado)

Así las rutas relativas y el mapa embebido se comportan igual que en producción:

```bash
# Con Python 3
python3 -m http.server 8080

# o con Node
npx serve .
```

Después entrá a <http://localhost:8080>.

### Opción C — Editar los estilos (SCSS → CSS)

El HTML usa `css/style.css`, que está compilado. Si vas a tocar el SCSS,
recompilalo:

```bash
# instalá Sass si no lo tenés
npm install -g sass

# compilado único
sass scss/style.scss css/style.css

# o en modo watch (recompila al guardar)
sass --watch scss/style.scss css/style.css
```

---

## 🗺️ Roadmap / ideas futuras

- [ ] Reemplazar el formulario de contacto por un backend real o servicio de mail.
- [ ] Carrito funcional (hoy `chart.html` es maquetado).
- [ ] Autenticación real en login/signup.
- [ ] Corregir las meta tags Open Graph (apuntan a rutas locales antiguas).

---

## 📄 Licencia

Sin licencia definida todavía. Uso educativo / portfolio personal.
