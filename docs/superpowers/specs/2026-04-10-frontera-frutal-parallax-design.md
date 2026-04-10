# Frontera Frutal — Parallax Scroll Presentation

**Date:** 2026-04-10
**Type:** Internal marketing presentation
**Format:** HTML/CSS single-page parallax scroll

---

## Objetivo

Showcase visual puro de los 3 productos de la línea Frontera Frutal. Mínimo texto, máximo impacto. Cada producto ocupa el mundo completo de la pantalla con sus colores propios extraídos de las etiquetas.

---

## Estructura de secciones

1. **Header fijo (sticky)** — Logo Frontera Frutal + GIF animado. `backdrop-filter: blur`. Z-index top.
2. **Hero (100vh)** — Intro de la línea. Fondo neutro oscuro. Logo grande centrado.
3. **Tropical (100vh)** — Mango & Passion Fruit. Paleta ámbar/dorado.
4. **Pink Paradise (100vh)** — Strawberry & Orange. Paleta rosa/coral.
5. **Summer Red (100vh)** — Apple & Orange. Paleta borgoña/rojo.
6. **Footer** — Fondo `#1A1A1A`, logo pequeño, tagline, espacio para links.

---

## Sistema de parallax (capas por sección)

| Capa | Elemento | Velocidad scroll |
|------|----------|-----------------|
| 1 | Fondo de color sólido | 0 (fijo) |
| 2 | Elementos de fruta/hojas | 0.3 (lento) |
| 3 | Splash de líquido | 0.6 (medio) |
| 4 | Botella principal | 1.0 (normal, ancla) |
| 5 | Partículas / bokeh | 1.4 (rápido, frente) |

---

## Paleta de colores (extraída de etiquetas)

| Producto | Color base | Color acento | Texto |
|----------|-----------|--------------|-------|
| Tropical | `#E8821A` | `#FFD166` | blanco |
| Pink Paradise | `#E8537A` | `#FFB5C8` | blanco |
| Summer Red | `#8B1A2B` | `#C0392B` | blanco |

---

## Transiciones entre secciones

- `scroll-driven animation` para morphing de color entre secciones
- Sin cortes abruptos — el color del fondo hace gradiente de uno al otro a medida que scrolleas
- Entrada de botella: fade-in + leve scale desde 0.85 → 1.0

---

## Placeholders para assets (fase 1 — esqueleto)

- Logo: rectángulo blanco con texto "FRONTERA FRUTAL"
- GIF header: rectángulo animado placeholder
- Botellas: rectángulos con color de la variante + nombre
- Frutas/elementos: círculos de colores en posiciones clave
- Videos: `<video>` tags vacíos con poster placeholder

---

## Tecnología

- HTML5 + CSS3 puro (sin frameworks)
- `position: sticky` para header
- `transform: translateY()` con `scroll-driven animations` o `IntersectionObserver` para parallax
- Sin dependencias externas — fácil de abrir en cualquier browser

---

## Assets disponibles en el proyecto

```
/LOGO FRUTAL.png
/1080x1080 portafolio.jpg
/FRUTILLA NARANJA/Frontera_PINK PARADISE_In-F.png
/MANGO MARACUYA/Frontera_TROPICAL_In-F.png
/MANZANA NARANJA/Frontera-Summer Red - frontal.png
```
