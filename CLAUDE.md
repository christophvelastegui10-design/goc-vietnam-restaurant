# CLAUDE.md — Creación de Páginas Web Profesionales

## Propósito

Este archivo guía a Claude para generar páginas web profesionales, visualmente memorables y funcionales. Cada proyecto debe reflejar intencionalidad de diseño, código limpio y una identidad estética clara.

---

## Flujo de Trabajo

### 1. Análisis del Proyecto

Antes de escribir una sola línea de código, responde estas preguntas:

- **¿Cuál es el propósito de la página?** (portafolio, SaaS, landing, blog, e-commerce, corporativa)
- **¿Quién es el usuario objetivo?** (edad, nivel técnico, contexto cultural)
- **¿Cuál es el tono deseado?** (formal, creativo, minimalista, audaz, lujoso)
- **¿Qué acción principal debe tomar el usuario?** (comprar, contratar, leer, registrarse)
- **¿Hay restricciones técnicas?** (framework, CMS, accesibilidad, SEO)

### 2. Dirección Estética

Elige UNA dirección y ejecútala con precisión. No mezcles estilos sin intención.

| Estilo | Características |
|--------|----------------|
| **Minimalista Refinado** | Espacio negativo generoso, tipografía elegante, paleta monocromática |
| **Maximalista Editorial** | Capas, superposiciones, tipografía expresiva, color saturado |
| **Brutalista/Raw** | Bordes crudos, grids rotos, contraste extremo, sin adornos |
| **Retro-Futurista** | Neón controlado, formas geométricas, referencias a los 80s/90s |
| **Orgánico/Natural** | Formas blandas, paleta tierra, texturas sutiles, tipografía humanista |
| **Corporativo Moderno** | Limpio, estructurado, confiable, iconografía clara |
| **Arte Digital/Experimental** | Animaciones generativas, WebGL, interacciones sorpresivas |

---

## Estándares de Código

### HTML Semántico

```html
<!-- CORRECTO: Estructura semántica -->
<header role="banner">
  <nav aria-label="Navegación principal">...</nav>
</header>
<main id="main-content">
  <section aria-labelledby="hero-heading">
    <h1 id="hero-heading">...</h1>
  </section>
</main>
<footer role="contentinfo">...</footer>

<!-- INCORRECTO: Divitis -->
<div class="header">
  <div class="nav">...</div>
</div>
```

### CSS — Variables y Sistema de Diseño

Siempre define un sistema de tokens al inicio del proyecto:

```css
:root {
  /* Colores */
  --color-primary: #0F172A;
  --color-accent: #6366F1;
  --color-surface: #F8FAFC;
  --color-text: #1E293B;
  --color-text-muted: #64748B;

  /* Tipografía */
  --font-display: 'Playfair Display', Georgia, serif;
  --font-body: 'DM Sans', system-ui, sans-serif;
  --font-mono: 'JetBrains Mono', monospace;

  /* Escala tipográfica */
  --text-xs: clamp(0.75rem, 1.5vw, 0.875rem);
  --text-sm: clamp(0.875rem, 1.8vw, 1rem);
  --text-base: clamp(1rem, 2vw, 1.125rem);
  --text-lg: clamp(1.125rem, 2.5vw, 1.25rem);
  --text-xl: clamp(1.25rem, 3vw, 1.5rem);
  --text-2xl: clamp(1.5rem, 4vw, 2rem);
  --text-3xl: clamp(2rem, 5vw, 3rem);
  --text-hero: clamp(2.5rem, 8vw, 5rem);

  /* Espaciado */
  --space-xs: 0.25rem;
  --space-sm: 0.5rem;
  --space-md: 1rem;
  --space-lg: 1.5rem;
  --space-xl: 2rem;
  --space-2xl: 3rem;
  --space-3xl: 5rem;

  /* Bordes */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 16px;
  --radius-xl: 24px;
  --radius-full: 9999px;

  /* Sombras */
  --shadow-sm: 0 1px 3px rgba(0,0,0,0.08);
  --shadow-md: 0 4px 16px rgba(0,0,0,0.10);
  --shadow-lg: 0 12px 40px rgba(0,0,0,0.15);

  /* Transiciones */
  --transition-fast: 150ms ease;
  --transition-base: 250ms ease;
  --transition-slow: 400ms cubic-bezier(0.4, 0, 0.2, 1);
}
```

### Tipografía — Reglas Críticas

```css
/* NUNCA usar: Arial, Roboto, Inter como primera opción */
/* SIEMPRE elegir fuentes con carácter para el display */

/* Pareja tipográfica de ejemplo (elegante) */
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&family=DM+Sans:wght@400;500&display=swap');

/* Pareja tipográfica de ejemplo (moderna/audaz) */
@import url('https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=Outfit:wght@400;500&display=swap');

/* Escala y ritmo */
h1 { font-size: var(--text-hero); line-height: 1.1; letter-spacing: -0.03em; }
h2 { font-size: var(--text-3xl);  line-height: 1.2; letter-spacing: -0.02em; }
h3 { font-size: var(--text-2xl);  line-height: 1.3; }
p  { font-size: var(--text-base); line-height: 1.75; }
```

---

## Secciones Esenciales por Tipo de Página

### Landing Page / SaaS

```
1. Hero         — Propuesta de valor clara, CTA principal, visual de impacto
2. Social Proof — Logos de clientes, número de usuarios, testimonios
3. Features     — 3-6 características clave con íconos/ilustraciones
4. How it Works — Proceso en 3 pasos (simplificado)
5. Pricing      — Máximo 3 planes, uno recomendado destacado
6. FAQ          — 5-8 preguntas frecuentes en accordion
7. Final CTA    — Llamada a acción de cierre con urgencia o valor
8. Footer       — Links, redes, legal, newsletter
```

### Portafolio / Freelance

```
1. Hero         — Nombre, rol, propuesta única, foto o visual
2. Trabajos     — Grid de proyectos con hover para detalles
3. Sobre mí     — Historia, habilidades, valores
4. Proceso      — Cómo trabajas con clientes
5. Testimonios  — 2-3 quotes con foto y nombre
6. Contacto     — Formulario simple o email directo
```

### Corporativa / Empresarial

```
1. Hero          — Misión de empresa, CTA secundario
2. Servicios     — Cards con íconos descriptivos
3. Nosotros      — Historia, valores, equipo
4. Casos de éxito — Métricas y resultados reales
5. Clientes      — Logos en banda horizontal
6. Blog/Recursos — 3 artículos recientes
7. Contacto/CTA  — Formulario de contacto o reunión
8. Footer        — Completo con sub-navegación
```

---

## Componentes UI — Patrones Recomendados

### Hero Section

```html
<section class="hero" aria-labelledby="hero-heading">
  <div class="hero__content">
    <p class="hero__eyebrow">Tagline breve aquí</p>
    <h1 id="hero-heading" class="hero__title">
      Propuesta de valor <em>irresistible</em>
    </h1>
    <p class="hero__subtitle">
      Subtítulo que complementa sin repetir. Máximo 2 líneas.
    </p>
    <div class="hero__actions">
      <a href="#" class="btn btn--primary">Acción Principal</a>
      <a href="#" class="btn btn--ghost">Ver Demo →</a>
    </div>
  </div>
  <div class="hero__visual" aria-hidden="true">
    <!-- Ilustración, screenshot de producto o video -->
  </div>
</section>
```

### Cards de Características

```html
<article class="feature-card">
  <div class="feature-card__icon" aria-hidden="true">
    <!-- SVG icon aquí -->
  </div>
  <h3 class="feature-card__title">Nombre de Feature</h3>
  <p class="feature-card__description">
    Descripción concisa del beneficio, no de la característica técnica.
  </p>
</article>
```

### Botones — Estados Completos

```css
.btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  border-radius: var(--radius-md);
  font-size: var(--text-sm);
  font-weight: 500;
  text-decoration: none;
  cursor: pointer;
  transition: all var(--transition-base);
  border: 2px solid transparent;
}

.btn--primary {
  background: var(--color-accent);
  color: white;
}

.btn--primary:hover {
  background: color-mix(in srgb, var(--color-accent) 85%, black);
  transform: translateY(-1px);
  box-shadow: 0 4px 16px color-mix(in srgb, var(--color-accent) 40%, transparent);
}

.btn--primary:active { transform: translateY(0); }

.btn--primary:focus-visible {
  outline: 3px solid var(--color-accent);
  outline-offset: 3px;
}
```

---

## Animaciones y Motion

### Principios

- **Propósito sobre decoración**: cada animación debe comunicar algo
- **Brevedad**: máximo 400ms para transiciones de UI, 800ms para reveals
- **Reducción de movimiento**: siempre respetar `prefers-reduced-motion`

```css
/* Animaciones de entrada */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(24px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes scaleIn {
  from { opacity: 0; transform: scale(0.95); }
  to   { opacity: 1; transform: scale(1); }
}

/* Escalonado para listas/grids */
.card:nth-child(1) { animation-delay: 0ms; }
.card:nth-child(2) { animation-delay: 80ms; }
.card:nth-child(3) { animation-delay: 160ms; }
.card:nth-child(4) { animation-delay: 240ms; }

/* Respeto a preferencias del usuario */
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

### Scroll-triggered Animations (Intersection Observer)

```javascript
const observer = new IntersectionObserver(
  (entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        entry.target.classList.add('is-visible');
        observer.unobserve(entry.target); // Anima solo una vez
      }
    });
  },
  { threshold: 0.1, rootMargin: '0px 0px -50px 0px' }
);

document.querySelectorAll('[data-animate]').forEach((el) => observer.observe(el));
```

---

## Responsive Design — Mobile First

```css
/* Breakpoints estándar */
/* mobile: 0-767px (base) */
/* tablet: 768px-1023px */
/* desktop: 1024px-1279px */
/* wide: 1280px+ */

/* Contenedor fluido */
.container {
  width: 100%;
  max-width: 1200px;
  margin-inline: auto;
  padding-inline: clamp(1rem, 5vw, 2rem);
}

/* Grid adaptable */
.grid-auto {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(min(280px, 100%), 1fr));
  gap: var(--space-lg);
}

/* Navbar responsive */
@media (max-width: 767px) {
  .nav__links {
    display: none;
    position: fixed;
    inset: 0;
    background: var(--color-primary);
    flex-direction: column;
    align-items: center;
    justify-content: center;
    z-index: 100;
  }

  .nav__links.is-open {
    display: flex;
  }
}
```

---

## Performance — Buenas Prácticas

### Imágenes

```html
<!-- Siempre con dimensiones + lazy loading + formato moderno -->
<picture>
  <source srcset="imagen.avif" type="image/avif">
  <source srcset="imagen.webp" type="image/webp">
  <img
    src="imagen.jpg"
    alt="Descripción clara y específica"
    width="800"
    height="600"
    loading="lazy"
    decoding="async"
  >
</picture>

<!-- Hero image: eager para LCP -->
<img src="hero.webp" alt="..." loading="eager" fetchpriority="high">
```

### Fuentes

```html
<!-- Preconnect y preload para fuentes críticas -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="preload" as="style" href="https://fonts.googleapis.com/css2?family=Syne:wght@700;800&display=swap">
```

### Critical CSS

- Inline CSS crítico en `<head>` (above-the-fold styles)
- Cargar CSS no crítico de forma diferida
- Evitar render-blocking resources

---

## Accesibilidad (WCAG 2.1 AA)

### Checklist Mínimo

- [ ] Contraste de color ≥ 4.5:1 para texto normal, ≥ 3:1 para texto grande
- [ ] Todos los elementos interactivos accesibles por teclado
- [ ] Focus visible con outline claro (nunca `outline: none` sin alternativa)
- [ ] Imágenes con `alt` descriptivo (o `alt=""` si son decorativas)
- [ ] Formularios con `<label>` asociados a cada input
- [ ] Estructura de headings lógica (h1 → h2 → h3, no saltos)
- [ ] Skip link "Saltar al contenido" al inicio del body
- [ ] ARIA roles solo cuando HTML semántico no es suficiente
- [ ] Textos de botones y enlaces descriptivos (no "clic aquí")

### Skip Navigation

```html
<a href="#main-content" class="skip-link">
  Saltar al contenido principal
</a>

<style>
.skip-link {
  position: absolute;
  transform: translateY(-100%);
  padding: 0.5rem 1rem;
  background: var(--color-accent);
  color: white;
  z-index: 9999;
  transition: transform var(--transition-fast);
}
.skip-link:focus {
  transform: translateY(0);
}
</style>
```

---

## SEO — Estructura Base

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Título Principal | Nombre del Sitio</title>
  <meta name="description" content="Descripción clara, 120-160 caracteres, con keywords.">

  <!-- Open Graph -->
  <meta property="og:title" content="Título Principal">
  <meta property="og:description" content="Descripción para redes sociales.">
  <meta property="og:image" content="https://misitio.com/og-image.jpg">
  <meta property="og:url" content="https://misitio.com">
  <meta property="og:type" content="website">

  <!-- Twitter Card -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="Título Principal">
  <meta name="twitter:image" content="https://misitio.com/twitter-card.jpg">

  <!-- Canonical -->
  <link rel="canonical" href="https://misitio.com/pagina-actual">

  <!-- Schema.org (JSON-LD) -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Organization",
    "name": "Nombre de Empresa",
    "url": "https://misitio.com",
    "logo": "https://misitio.com/logo.png"
  }
  </script>
</head>
```

---

## Dark Mode

```css
/* Sistema de temas con CSS variables */
:root {
  color-scheme: light;
  --bg: #FFFFFF;
  --bg-surface: #F8FAFC;
  --text: #0F172A;
  --text-muted: #64748B;
  --border: rgba(15, 23, 42, 0.1);
}

@media (prefers-color-scheme: dark) {
  :root {
    color-scheme: dark;
    --bg: #0F172A;
    --bg-surface: #1E293B;
    --text: #F8FAFC;
    --text-muted: #94A3B8;
    --border: rgba(248, 250, 252, 0.1);
  }
}

/* Toggle manual (cuando el usuario puede elegir) */
[data-theme="dark"] {
  --bg: #0F172A;
  /* ... */
}
```

---

## Formularios — UX Óptimo

```html
<form novalidate>
  <div class="field">
    <label for="email" class="field__label">
      Correo electrónico <span aria-label="requerido">*</span>
    </label>
    <input
      type="email"
      id="email"
      name="email"
      class="field__input"
      placeholder="tu@ejemplo.com"
      autocomplete="email"
      required
      aria-describedby="email-error"
    >
    <span
      id="email-error"
      class="field__error"
      role="alert"
      aria-live="polite"
      hidden
    >
      Por favor ingresa un correo válido.
    </span>
  </div>

  <button type="submit" class="btn btn--primary">
    Enviar mensaje
  </button>
</form>
```

---

## Anti-Patrones — Lo que NUNCA hacer

### Diseño

- ❌ Gradiente morado sobre fondo blanco (el cliché IA)
- ❌ Tipografías genéricas (Inter, Roboto) como primera opción
- ❌ Sombras de caja en todo (shadow soup)
- ❌ Más de 3 colores primarios sin sistema
- ❌ Animaciones en loop sin control del usuario
- ❌ Hero con imagen de stock genérica de personas sonriendo

### Código

- ❌ `!important` para parchar especificidad
- ❌ `position: absolute` sin `position: relative` en padre
- ❌ Anchos en px para contenedores (`width: 1200px` → `max-width: 1200px`)
- ❌ `margin: 0 auto` sin definir ancho del elemento
- ❌ JavaScript inline en atributos HTML (`onclick="..."`)
- ❌ Imágenes sin `width` y `height` (causa CLS)
- ❌ `outline: none` sin alternativa de focus visible

### Performance

- ❌ Cargar fuentes sin `font-display: swap`
- ❌ Imágenes PNG pesadas donde debería haber WebP/AVIF
- ❌ Scripts síncronos en `<head>` sin `defer` o `async`
- ❌ CSS no utilizado sin purgar

---

## Estructura de Archivos Recomendada

```
proyecto/
├── index.html
├── assets/
│   ├── css/
│   │   ├── tokens.css       # Variables de diseño
│   │   ├── base.css         # Reset + estilos base
│   │   ├── components.css   # Componentes UI
│   │   ├── layout.css       # Grid, container, secciones
│   │   └── utilities.css    # Clases de utilidad
│   ├── js/
│   │   ├── main.js          # Lógica principal
│   │   ├── animations.js    # Intersection Observer, GSAP
│   │   └── forms.js         # Validación y envío
│   ├── images/
│   │   ├── hero/
│   │   ├── icons/
│   │   └── og/              # Imágenes para redes sociales
│   └── fonts/               # Fuentes auto-hospedadas (opcional)
├── pages/                   # Páginas adicionales
└── favicon.ico
```

---

## Checklist Final antes de Entregar

### Funcional

- [ ] Navegación funciona en mobile y desktop
- [ ] Formularios validan y muestran errores claros
- [ ] Links internos y externos funcionan
- [ ] No hay errores en consola del navegador

### Visual

- [ ] Revisado en Chrome, Firefox y Safari
- [ ] Revisado en móvil real (no solo DevTools)
- [ ] Dark mode se ve bien si está implementado
- [ ] No hay texto desbordado ni elementos rotos

### Performance (Lighthouse ≥ 90)

- [ ] LCP < 2.5s
- [ ] CLS < 0.1
- [ ] FID / INP < 200ms
- [ ] Sin recursos bloqueantes críticos

### Accesibilidad

- [ ] Navegación completa por teclado (Tab, Enter, Escape)
- [ ] Screen reader no anuncia elementos decorativos
- [ ] Contraste verificado con herramienta (WebAIM, Stark)

### SEO

- [ ] Meta title y description únicos
- [ ] Open Graph configurado
- [ ] Canonical URL definida
- [ ] Sitemap.xml generado (si aplica)

---

## Recursos de Referencia

| Recurso | Uso |
|---------|-----|
| MDN Web Docs | Referencia HTML/CSS/JS |
| Can I Use | Compatibilidad de browsers |
| WebAIM Contrast Checker | Contraste de color |
| Google Fonts | Tipografías web |
| Squoosh | Optimización de imágenes |
| PageSpeed Insights | Métricas de performance |
| WAVE | Auditoría de accesibilidad |
| JSON-LD Playground | Schema.org testing |

---

*Última actualización: Abril 2026 — Para uso con Claude Sonnet 4.6*
