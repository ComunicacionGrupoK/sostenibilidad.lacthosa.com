# Memoria de Sostenibilidad Sula 2023-2024

Sitio web estático para presentar la **Memoria de Sostenibilidad Sula 2023-2024** bajo el concepto **Pulso Responsable: Cada Acción Cuenta**.

El proyecto muestra una landing page con identidad visual de Lacthosa/Sula, acceso a una memoria digital tipo flipbook y un botón para descargar el PDF oficial.

## Sitio

https://sostenibilidad.lacthosa.com

## Vista general

El sitio incluye:

- Encabezado con logos institucionales.
- Sección principal con imagen de campaña.
- Botón para ver la memoria en línea.
- Botón para descargar la memoria en PDF.
- Iframe embebido con flipbook digital.
- SEO básico.
- Open Graph.
- Datos estructurados para Google, redes sociales y LLMs.

## Tecnologías utilizadas

- HTML
- CSS
- JavaScript
- Node.js
- npm
- serve

## Requisitos previos

Antes de ejecutar el proyecto, asegúrate de tener instalado:

- Node.js
- npm

Puedes verificarlo con:

```bash
node -v
npm -v
```

## Instalación

Entra a la carpeta del proyecto:

```bash
cd memoria-sostenibildiad
```

Instala las dependencias:

```bash
npm install
```

## Levantar el proyecto en local

Ejecuta:

```bash
npm start
```

El proyecto se levantará como sitio estático.

Normalmente estará disponible en:

```txt
http://localhost:3000
```

Si la terminal muestra otro puerto, utiliza el puerto indicado.

## Levantar en un puerto específico

También puedes levantarlo manualmente en el puerto `3000`:

```bash
npx serve -s . -l 3000
```

Luego abre en el navegador:

```txt
http://localhost:3000
```

## Scripts disponibles

```json
{
    "scripts": {
        "start": "npx serve -s",
        "build": "echo 'No build step'"
    }
}
```

### npm start

Levanta el sitio en local usando `serve`.

### npm run build

Actualmente no genera archivos de producción porque el proyecto es HTML/CSS estático y no requiere proceso de compilación.

## Estructura del proyecto

```txt
memoria-sostenibildiad/
├── css/
│   └── main.css
├── images/
│   ├── logoLactohsa.svg
│   ├── 2324.svg
│   ├── isologo.svg
│   ├── logoPulse.svg
│   ├── favicon.ico
│   ├── webclip.png
│   └── opengraph.png
├── index.html
├── package.json
├── package-lock.json
├── README.md
└── .gitignore
```

## Archivo principal

El archivo principal del sitio es:

```txt
index.html
```

Ahí se encuentra la estructura de la landing page, los metadatos SEO/Open Graph, los botones principales y el iframe de la memoria digital.

## Memoria digital

La memoria se muestra mediante un iframe embebido desde Heyzine:

```html
<iframe
    src="https://heyzine.com/flip-book/73a86c67f7.html#page/1"
    class="flipbook-iframe"
    frameborder="0"
    allowfullscreen
>
</iframe>
```

## Descarga de PDF

El botón de descarga apunta al PDF alojado en Supabase Storage:

```txt
https://wtzcjehvfofuphkmvsru.supabase.co/storage/v1/object/public/storage/MemoriaSostenibilidad_2023-2024_.pdf
```

## SEO y Open Graph

El sitio incluye metadatos para mejorar su visualización en buscadores y redes sociales:

- Title
- Description
- Canonical URL
- Open Graph
- Twitter Card
- Datos estructurados JSON-LD
- Imagen de previsualización en `images/opengraph.png`

Se recomienda que la imagen Open Graph tenga tamaño:

```txt
1200 x 630 px
```

## Despliegue

Este proyecto puede desplegarse en:

- Vercel
- Netlify
- GitHub Pages
- Hosting tradicional
- Servidor propio con Apache o Nginx

Como es un sitio estático, solo necesitas publicar los archivos de la raíz del proyecto.

## Recomendaciones antes de publicar

Antes de subir a producción, revisar:

- Que `index.html` esté en la raíz.
- Que `css/main.css` cargue correctamente.
- Que todas las imágenes existan dentro de la carpeta `images`.
- Que `images/opengraph.png` exista.
- Que la imagen Open Graph sea de `1200x630`.
- Que el dominio configurado en los metadatos SEO sea el dominio final.
- Que el enlace al PDF funcione.
- Que el iframe de Heyzine cargue correctamente.
- Que el sitio se vea bien en móvil.

## Notas importantes

Si cambia el dominio final, actualizar en `index.html` las siguientes líneas:

```html
<link rel="canonical" href="https://sostenibilidad.lacthosa.com/" />
<meta property="og:url" content="https://sostenibilidad.lacthosa.com/" />
<meta
    property="og:image"
    content="https://sostenibilidad.lacthosa.com/images/opengraph.png"
/>
<meta
    name="twitter:image"
    content="https://sostenibilidad.lacthosa.com/images/opengraph.png"
/>
```

## Créditos

Proyecto desarrollado para la presentación digital de la **Memoria de Sostenibilidad Sula 2023-2024**.

Concepto: **Pulso Responsable: Cada Acción Cuenta**.
