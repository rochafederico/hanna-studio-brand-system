# HANNA Studio — Sistema Visual v1

**Versión:** 1.0.0  
**Fecha de actualización:** 2026-04-02  
**Responsable:** Equipo de diseño HANNA Studio

---

## Tabla de contenidos

1. [Principios visuales](#1-principios-visuales)
2. [Sistema de logo](#2-sistema-de-logo)
3. [Sistema de isotipo](#3-sistema-de-isotipo)
4. [Sistema cromático](#4-sistema-cromático)
5. [Sistema tipográfico](#5-sistema-tipográfico)
6. [Sistema de proporciones](#6-sistema-de-proporciones)
7. [Sistema de composición](#7-sistema-de-composición)
8. [Sistema de formas](#8-sistema-de-formas)
9. [Design tokens](#9-design-tokens)
10. [Cómo usar este documento](#10-cómo-usar-este-documento)
11. [Changelog](#11-changelog)

---

## 1. Principios visuales

La identidad debe comunicar:

- **Elegancia:** contraste tipográfico y espacios amplios
- **Feminidad:** tonos suaves + formas curvas
- **Premium:** minimalismo, mucho aire, pocos elementos
- **Modernidad:** composiciones limpias y digitales
- **Escalabilidad:** adaptable a redes, WhatsApp y UI

**Regla clave:** menos elementos, más jerarquía.

---

## 2. Sistema de logo

> Archivo de referencia: [`assets/logos/logo.svg`](../assets/logos/logo.svg)

### Estructura

```
HANNA       ← Bodoni Moda, uppercase, grafito #2F2B34
──────────  ← separación vertical: 105 px (en canvas 1200×600)
STUDIO      ← Montserrat SemiBold, rosa acento #C899B3
```

### Especificaciones tipográficas

| Elemento | Fuente | Peso | Letter-spacing | Color |
|----------|--------|------|----------------|-------|
| HANNA | Bodoni Moda | 400 (Regular) | +6 px | `#2F2B34` |
| STUDIO | Montserrat | 600 (SemiBold) | +8 px | `#C899B3` |

### Tamaños mínimos de uso

| Soporte | Tamaño mínimo |
|---------|---------------|
| Digital (pantalla) | 120 px de ancho |
| Redes sociales (avatar/miniatura) | usar isotipo en lugar del logo completo |
| Impresión | 30 mm de ancho |
| Favicon / ícono de app | usar isotipo |

### Usos incorrectos

- ❌ No usar sobre fondos oscuros sin versión alternativa en blanco
- ❌ No distorsionar las proporciones del logo (stretch horizontal o vertical)
- ❌ No cambiar los colores por fuera de la paleta oficial
- ❌ No aplicar efectos (sombras, gradientes, bordes) sobre el logo
- ❌ No usar Bodoni Moda en peso distinto al 400

---

## 3. Sistema de isotipo

> Archivo de referencia: [`assets/logos/isologo.svg`](../assets/logos/isologo.svg)

### Estructura y proporciones

El isotipo es un monograma circular construido sobre un canvas de **512 × 512 px**:

| Elemento | Valor |
|----------|-------|
| Canvas | 512 × 512 px |
| Círculo contenedor | radio 150 px (58.6% del canvas), centrado en 256, 256 |
| Grosor del aro | 8 px, color rosa nude `#E8DCDC` |
| Monograma "H" | Bodoni Moda 400, 180 px, color grafito `#2F2B34` |
| Fondo | Marfil suave `#F8F4F2` |

### Contextos de uso

El isotipo se usa en lugar del logo completo cuando el espacio disponible es reducido o cuadrado:

- ✅ Favicon (16 × 16 px, 32 × 32 px)
- ✅ Avatar de redes sociales (Instagram, WhatsApp, TikTok)
- ✅ Sello o marca de agua en fotografías
- ✅ Ícono de aplicación móvil
- ✅ Bordado o estampado en textiles (espacio < 30 mm)

---

## 4. Sistema cromático

### Paleta principal

| Rol | Nombre | HEX | RGB | HSL |
|-----|--------|-----|-----|-----|
| Primary | Grafito elegante | `#2F2B34` | 47, 43, 52 | 266°, 9%, 19% |
| Secondary | Rosa nude | `#E8DCDC` | 232, 220, 220 | 0°, 21%, 89% |
| Accent | Rosa acento | `#C899B3` | 200, 153, 179 | 327°, 30%, 69% |
| Background | Marfil suave | `#F8F4F2` | 248, 244, 242 | 20°, 31%, 96% |

### Contraste WCAG

| Combinación | Ratio | Nivel WCAG |
|-------------|-------|-----------|
| Grafito `#2F2B34` sobre Marfil `#F8F4F2` | 11.3:1 | **AAA** ✅ |
| Grafito `#2F2B34` sobre Rosa nude `#E8DCDC` | 9.2:1 | **AAA** ✅ |
| Grafito `#2F2B34` sobre Rosa acento `#C899B3` | 5.1:1 | **AA** ✅ |
| Rosa acento `#C899B3` sobre Marfil `#F8F4F2` | 2.2:1 | **Falla** ⚠️ — solo usar en textos grandes (≥ 18 px Bold) o decorativos |

### Cuándo usar cada color

| Color | Uso principal |
|-------|---------------|
| Grafito `#2F2B34` | Texto de cuerpo, titulares, ícono en fondos claros |
| Rosa nude `#E8DCDC` | Fondos secundarios, divisores, marcos decorativos |
| Rosa acento `#C899B3` | CTAs, descriptor "STUDIO", detalles de isotipo, highlights |
| Marfil `#F8F4F2` | Fondo principal de todas las piezas |

---

## 5. Sistema tipográfico

### Fuentes principales

| Rol | Fuente | Fallback web | Fuente |
|-----|--------|--------------|--------|
| Brand / Titulares | Bodoni Moda | `'Didot', 'Georgia', serif` | Google Fonts |
| UI / Comunicación | Montserrat | `'Arial', 'Helvetica', sans-serif` | Google Fonts |

### Escala tipográfica

| Nivel | Uso | Fuente | Peso | Tamaño | Letter-spacing |
|-------|-----|--------|------|--------|----------------|
| Display | Nombre de marca "HANNA" | Bodoni Moda | 400 | 160 px (SVG) / clamp(48px, 10vw, 160px) | +6 px |
| H1 | Titulares principales | Bodoni Moda | 400 | 48–72 px | +2 px |
| H2 | Subtítulos de sección | Montserrat | 600 | 28–36 px | +1 px |
| Label | Descriptor "STUDIO" / etiquetas | Montserrat | 600 | 74 px (SVG) / 14–18 px (UI) | +8 px |
| Body | Texto de cuerpo | Montserrat | 400 | 14–16 px | 0 |
| Caption | Leyendas, precios, hashtags | Montserrat | 400 | 11–13 px | +1 px |
| CTA | Botones, llamadas a acción | Montserrat | 600 | 13–15 px | +3 px |

### Pesos usados

- **Bodoni Moda 400** — exclusivo para el nombre de marca y titulares editoriales
- **Montserrat 400** — cuerpo de texto y captions
- **Montserrat 600 (SemiBold)** — descriptor, labels, CTAs, subtítulos

---

## 6. Sistema de proporciones

Las proporciones de color en cada pieza visual:

- **60%** → fondos claros (Marfil `#F8F4F2`)
- **25%** → estructura y texto (Grafito `#2F2B34`)
- **15%** → acentos y CTA (Rosa acento `#C899B3`)

---

## 7. Sistema de composición

### Reglas de espacio en torno al logo

El logo debe tener una zona de protección mínima equivalente a la altura de la letra "H" del logotipo a cada lado.

```
         [ zona de protección ]
[zp]  HANNA         [zp]
[zp]  STUDIO        [zp]
         [ zona de protección ]
```

### Casos de uso concretos

#### Post de Instagram (1080 × 1080 px)
```
[Fondo marfil — 60% del espacio]

   [logo centrado — zona superior o inferior]

   PROMO DEL MES

   20% OFF

   [CTA] reservá tu turno
```
- Logo en la zona superior tercio o inferior tercio
- Texto centrado con Montserrat
- Margen interior mínimo: 80 px en todos los lados

#### Historia de Instagram / WhatsApp (1080 × 1920 px)
- Logo o isotipo en la esquina superior izquierda (margen 60 px)
- Contenido principal centrado verticalmente
- Nunca superponer el logo sobre fotografías sin zona de protección

#### Header de sitio web (full-width)
- Logo alineado a la izquierda, centrado verticalmente en el header
- Altura del header: mínimo 72 px
- Logo a no más del 50% de la altura del header
- Ancho mínimo del logo en header: 120 px

#### Portada de WhatsApp Business (1920 × 1080 px)
- Logo centrado, tamaño medio (≈ 400 px de ancho)
- Fondo Marfil suave
- Sin texto adicional, solo logo e isotipo si aplica

---

## 8. Sistema de formas

Los elementos gráficos decorativos de la marca se basan en:

- **Círculos** — contenedor del isotipo, marcos decorativos
- **Arcos suaves** — divisores, detalles de composición
- **Líneas finas** — separadores horizontales flanqueando el logo (2 px, color `#E8DCDC`)
- **Curvas tipo pestaña / ceja** — detalle opcional en la parte inferior del isotipo

---

## 9. Design tokens

Los tokens completos están disponibles en formato JSON en [`tokens/brand-tokens.json`](../tokens/brand-tokens.json).

### Resumen de tokens

| Categoría | Token | Valor |
|-----------|-------|-------|
| Color | `color.primary` | `#2F2B34` |
| Color | `color.secondary` | `#E8DCDC` |
| Color | `color.accent` | `#C899B3` |
| Color | `color.background` | `#F8F4F2` |
| Fuente | `font.brand` | `Bodoni Moda` |
| Fuente | `font.ui` | `Montserrat` |
| Tamaño | `fontSize.display` | `160px` |
| Tamaño | `fontSize.h1` | `56px` |
| Tamaño | `fontSize.h2` | `32px` |
| Tamaño | `fontSize.label` | `14px` |
| Tamaño | `fontSize.body` | `15px` |
| Tamaño | `fontSize.caption` | `12px` |
| Peso | `fontWeight.regular` | `400` |
| Peso | `fontWeight.semibold` | `600` |
| Tracking | `letterSpacing.brand` | `6px` |
| Tracking | `letterSpacing.descriptor` | `8px` |
| Tracking | `letterSpacing.cta` | `3px` |
| Spacing | `spacing.xs` | `4px` |
| Spacing | `spacing.sm` | `8px` |
| Spacing | `spacing.md` | `16px` |
| Spacing | `spacing.lg` | `32px` |
| Spacing | `spacing.xl` | `64px` |
| Spacing | `spacing.logoProtection` | `80px` |
| Border radius | `borderRadius.circle` | `9999px` |
| Border radius | `borderRadius.card` | `12px` |
| Border radius | `borderRadius.button` | `6px` |

---

## 10. Cómo usar este documento

Este archivo es la **fuente de verdad** del sistema visual de HANNA Studio.

- Cualquier cambio en colores, tipografías o componentes debe reflejarse primero aquí y luego propagarse a los demás archivos (`tokens/brand-tokens.json`, archivos SVG, Figma).
- Para proponer un cambio, abrir un Pull Request con la modificación documentada en el [Changelog](#11-changelog).
- Las versiones anteriores se conservan en el historial de Git.
- El archivo `tokens/brand-tokens.json` se genera a partir de este documento y puede consumirse directamente por herramientas como Figma Tokens, Style Dictionary o variables CSS.

---

## 11. Changelog

| Versión | Fecha | Cambios |
|---------|-------|---------|
| 1.0.0 | 2026-04-02 | Versión inicial: principios visuales, logo, isotipo, paleta, tokens básicos |
