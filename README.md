# Grupo Leos — sitio web para Render

Esta entrega es **un sitio NUEVO e independiente**. No reemplaza el sitio que ya existe en `https://colchones-leos.onrender.com`.

## Qué incluye
- Una página corporativa de **Grupo Leos** con dos líneas: **Muebles Tubulares Leos** y **Colchones Leos**.
- Catálogo tubular interactivo con **45 fotografías reales** del PDF proporcionado.
- Filtros por categorías, búsqueda de modelos, fichas con detalles y enlace a PDF descargable.
- Presentación de Colchones Leos con imagen real recuperada y enlace al sitio ORIGINAL. El catálogo de colchones existente NO se incluyó porque el ZIP recibido estaba cortado.
- Diseño adaptable para celulares y computadoras, sin dependencias y sin necesidad de compilar.
- Botones de copiar mensajes de cotización (no envían WhatsApp automáticamente porque **no se proporcionó el número de Grupo Leos**).

## Publicar sin afectar tu web actual
1. Descomprime este ZIP.
2. En GitHub crea un **repositorio nuevo** (por ejemplo `grupo-leos-web`).
3. Sube el contenido de la carpeta extraída: `dist`, `render.yaml` y `README.md`. No subas el ZIP como archivo del repositorio.
4. En https://dashboard.render.com elige **New → Static Site** y conecta el repositorio nuevo.
5. Si Render pregunta: **Build Command** `echo ready` (o `true`); **Publish Directory** `dist`. Si usas Blueprint, `render.yaml` ya describe el servicio.
6. Publica y prueba búsquedas, fotografías, PDF y enlace de Colchones Leos.
7. **NO** elimines ni cambies el servicio `colchones-leos` hasta revisar la nueva versión.

## Configurar WhatsApp para cotizaciones
Abre `dist/app.js`, en la segunda sección verás:

`const WHATSAPP_GRUPO_LEOS = "";`

Escribe el número validado con clave de país, sin `+` ni espacios. Por ejemplo, la estructura en México sería `52XXXXXXXXXX` (es un **ejemplo de formato**, NO un número real). Antes de configurarlo, los botones copian un texto de solicitud, para que puedas mandarlo a tu representante.

## Verificación de Meta: pendientes necesarios
Esta versión muestra explícitamente la relación comercial entre las marcas, pero no sustituye los documentos oficiales ni garantiza la verificación. Antes de enviar a Meta, agrega con autorización del titular los datos legales/comerciales verificables que correspondan a su Constancia de Situación Fiscal (nombre completo, domicilio, teléfono, etc., según aplique y convenga publicar). No inventes la razón social de una persona física ni uses `Grupo Leos` como nombre legal si la constancia contiene el nombre de una persona.

## ZIP anterior: incompleto
El ZIP recibido contenía un segundo ZIP interno con una descarga parcial: faltaba su directorio central y la mayor parte de la distribución, incluido el PDF de colchones de ~24 MB. No es seguro recrear la web original a partir de ese archivo. Para integrarlo todo en una sola página, vuelve a descargar el repositorio original en GitHub: `Code → Download ZIP`, y comprueba que la descarga terminó antes de subirlo.

## Carpetas
- `dist/index.html`: página principal.
- `dist/styles.css`: estilos.
- `dist/app.js`: lógica de filtros y cotizaciones.
- `dist/assets/tubulares`: las 45 fotografías reales de muebles tubulares.
- `dist/assets/colchones`: imágenes recuperadas del ZIP incompleto.
- `dist/catalogos`: catálogo tubular original en PDF.
- `dist/data/productos.json`: datos estructurados de las fichas.
