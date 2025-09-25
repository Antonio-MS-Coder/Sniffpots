# Landing Page – Sniff Pots (Fit Mental)
Repositorio: https://github.com/Antonio-MS-Coder/Sniffpots.git  
Dominio: sniffpot.crissteinman.com (subdominio de crissteinman.com)  
Sitio madre: https://crissteinman.com

## Resumen
Landing minimalista, rápida y responsive para presentar Sniff Pots (aromaterapia portátil), con:
1) catálogo de variedades (Focus, Respirus, Serenus, Noctus) + Kit,  
2) **registro rápido para mayoristas** (Google Forms),  
3) placeholders para integrar **Stripe** (compras y fee de inscripción) en la siguiente iteración.

---

## Variables del proyecto (ya definidas)
- `REGISTRO_FORM_URL`: **https://forms.gle/RxyWPJ6LzsAFKFpP8**  
  - *Embed opcional (recomendado en modal/section):* `https://docs.google.com/forms/d/e/<FORM_ID>/viewform?embedded=true`  
    > Nota: si usas el short link, entra al editor del Form y copia el **Embed HTML** para obtener el `<FORM_ID>` y usar `viewform?embedded=true`.
- `CONTACT_WHATSAPP_URL`: **https://wa.me/525618532322**  
  - (Formato internacional sin espacios; MX = `52` + número de 10 dígitos)
- `CONTACT_EMAIL`: **mailto:gerentecomercial@lck.com.mx**
- `CUSTOM_DOMAIN`: `sniffpot.crissteinman.com`

> **Nota:** En esta versión NO se integra Stripe; deja botones y hooks preparados (`data-product-id`, `data-sku`, etc.) para la siguiente iteración.

---

## Estructura de secciones (Wireframe → HTML/React/Tailwind)
### 1) Hero
- **H1:** “Aromaterapia portátil para cada momento de tu día.”
- **H2:** “Lleva contigo la calma, la energía o el enfoque que necesitas en segundos.”
- **CTAs:**
  - `Conoce las variedades` → scroll a `#productos`
  - `Registro mayorista` → abre **https://forms.gle/RxyWPJ6LzsAFKFpP8** en nueva pestaña o modal embebido

### 2) Qué son (id: #que-son)
“Sniff Pots son cajitas de aromaterapia diseñadas para tu estilo de vida ajetreado. Cada caja contiene perlas aromáticas con mezclas especiales que puedes llevar a cualquier lugar. Solo ábrela, inhala y disfruta los beneficios.”

Steps con iconografía (line icons): **Abre → Inhala → Equilíbrate**

### 3) Productos / Variedades (id: #productos)
Grid de 5 cards (4 individuales + 1 kit destacado). Cada card:
- Imagen (ver **Assets**)
- Nombre + descripción corta
- Precio (si aplica en esta fase pública)
- Botones:
  - “Comprar [Variedad]” → (placeholder Stripe: `data-product-id="focus"`, etc.)
  - “Ver detalles” → modal con descripción extendida

**Variedades (copy corto):**
- **Focus**: Energizante para concentración/claridad (viajes, trabajo, exámenes, conferencias).
- **Respirus**: Relajante profundo; descanso y sueño reparador; ideal rutina nocturna.
- **Serenus**: Alivia tensión y restaura equilibrio; ideal para días ajetreados.
- **Noctus**: Facilita el sueño; calma y reconforta; ideal para viajes o el hogar.
- **Kit 4** (destacado): las cuatro variedades en un solo set a precio especial.

### 4) Precios y Ofertas (id: #precios)
| Producto         | Precio normal | Precio LCK | Mayoreo |
|------------------|---------------|------------|---------|
| Caja individual  | $250          | $200       | $150    |
| Kit 4 variedades | $800          | $650       | —       |

**Botones (placeholder):**
- “Comprar individual”
- “Comprar kit”
- “Registro a mayoreo” → **https://forms.gle/RxyWPJ6LzsAFKFpP8**

### 5) Registro Mayorista (id: #mayoreo)
- Beneficios: acceso a precio preferencial ($150/caja), compras por volumen, soporte de materiales POP.
- Botón primario: **“Registrarme como mayorista”** → **https://forms.gle/RxyWPJ6LzsAFKFpP8**  
- **Opción embebida (iframe en modal/section):** usar el Embed oficial del Form.

### 6) Testimonios (id: #testimonios)
- “Me ayudó a concentrarme antes de mis exámenes.” – Estudiante  
- “Mi pausa de calma en días pesados.” – Ejecutiva  
- “Ideal para viajes; me relaja en avión.” – Viajero frecuente

### 7) FAQ (id: #faq)
- ¿Cuánto dura un Sniff Pot?  
- ¿Es seguro para niños?  
- ¿Se puede llevar en avión?  
- ¿Cómo usarlo correctamente?

### 8) Footer
- Logos: Fit Mental + Sniff Pots  
- Enlaces: Términos, Privacidad  
- Contacto: **WhatsApp** (https://wa.me/525618532322) y **Email** (gerentecomercial@lck.com.mx)

---

## Estilo visual
- **Paleta:**
  - Verde salvia `#A3B18A`
  - Lavanda `#B7A2CC`
  - Beige claro `#FDF6EC`
  - Azul profundo `#264653`
- **Tipografía:** Sans serif elegante (Inter/Manrope/Outfit).  
- **Estética:** Minimal, editorial, wellness (aire, sombras suaves, esquinas 2xl).

---

## Assets a generar (nombres + tamaños)
Guardar en `assets/` y referenciar en código.

1. **Hero**  
   - `assets/hero_sniffpots_1792x1024.jpg`
2. **Iconos 3 pasos** (PNG transparente, line-art)  
   - `assets/icon_open_512.png`  
   - `assets/icon_inhale_512.png`  
   - `assets/icon_balance_512.png`
3. **Variedades** (pack coherente, 1024×1024)  
   - `assets/product_focus_1024.png` (fondo naranja energía)  
   - `assets/product_respirus_1024.png` (fondo azul relax)  
   - `assets/product_serenus_1024.png` (fondo verde suave)  
   - `assets/product_noctus_1024.png` (fondo lavanda/azul noche)
4. **Kit**  
   - `assets/product_kit_1024.png` (4 juntas, fondo beige con sombra)
5. **Testimonios (plantilla)**  
   - `assets/testimonial_bg_800.png` (pastel simple)

---

## Copys (listos para pegar)
**Hero H1:** Aromaterapia portátil para cada momento de tu día.  
**Hero H2:** Lleva contigo la calma, la energía o el enfoque que necesitas en segundos.

**Qué son (párrafo):**  
Sniff Pots son cajitas de aromaterapia diseñadas para tu estilo de vida ajetreado. Cada caja contiene perlas aromáticas con mezclas especiales que puedes llevar a cualquier lugar. Solo ábrela, inhala y disfruta los beneficios.

**Variedades – descripciones cortas (arriba en §3).**

**Registro mayorista (beneficios):**  
- Acceso a precio preferencial ($150 por caja)  
- Compras por volumen con disponibilidad prioritaria  
- Soporte de materiales para tu punto de venta

**Contacto:**  
- WhatsApp: https://wa.me/525618532322  
- Email: gerentecomercial@lck.com.mx

---

## Arquitectura técnica (v1 sin Stripe)
- Static site con **HTML + Tailwind** o **Vite + React + Tailwind** (elige).  
- Registro mayorista vía **Google Forms** (link/iframe).  
- Preparar data-attributes para Stripe (futura iteración):
  - `data-product-id="focus|respirus|serenus|noctus|kit"`
  - `data-action="buy"` o `data-action="wholesale-fee"`
- Accesibilidad: foco visible, alt text, contraste AA.

---

## Estructura de carpetas
/
├─ index.html (o /src/main.jsx si usas React)
├─ /assets
│  ├─ hero_sniffpots_1792x1024.jpg
│  ├─ icon_open_512.png
│  ├─ icon_inhale_512.png
│  ├─ icon_balance_512.png
│  ├─ product_focus_1024.png
│  ├─ product_respirus_1024.png
│  ├─ product_serenus_1024.png
│  ├─ product_noctus_1024.png
│  └─ product_kit_1024.png
├─ /styles (si aplican)
└─ CNAME  (una sola línea: sniffpot.crissteinman.com)