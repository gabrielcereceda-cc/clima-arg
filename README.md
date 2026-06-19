# clima-arg

Dashboard web de bandas de temperatura para Argentina.

## Stack
- Frontend estático (HTML + Plotly.js) — sin build steps
- API: [Open-Meteo](https://open-meteo.com) — gratuita, sin API key
- Hosting: Cloudflare Pages

## Deploy en Cloudflare Pages

1. Subir este repo a GitHub
2. Ir a [Cloudflare Pages](https://pages.cloudflare.com) → Create a project
3. Conectar el repo `clima-arg`
4. Configuración de build:
   - **Framework preset**: None
   - **Build command**: *(vacío)*
   - **Build output directory**: `/` (raíz)
5. Deploy → URL: `clima-arg.pages.dev`

## Estructura

```
clima-arg/
├── index.html    ← app completa
└── README.md
```

## Configuración

Todos los parámetros editables están al inicio del `<script>` en `index.html`:

```js
const CIUDADES = [...]          // ciudades y coordenadas
const OLA_POLAR = {...}         // bandas de referencia fijas
const COLORES = {...}           // paleta de colores
```

## Etapas de desarrollo

- [x] Etapa 1 — Pronóstico 7 días, selector ciudades/fechas, bandas
- [ ] Etapa 2 — Histórico (Cloudflare Worker + KV)
- [ ] Etapa 3 — Récords, alertas, exportar imagen
