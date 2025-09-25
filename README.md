# C.D. Talentos Arequipa — Sitio Web

Sitio web estático desarrollado para la Academia de Vóley “C.D. Talentos Arequipa”, orientado a difundir información institucional (sede, horarios, enfoque formativo) y ofrecer un canal de contacto accesible. El proyecto prioriza accesibilidad, estructura semántica, diseño responsivo y una implementación limpia con HTML5, CSS/SASS, JavaScript (vanilla) y Bootstrap 5.

## Integrantes
- Lazo Franco, Mauricio Paolo
- Lonasco Santamarina, Leonardo Oliver
- Reaño Soto, Iván Edgardo

---

## Temática del sitio

- Página de inicio (`index.html`): presentación del club, pilares (niveles, metodología y valores) y llamado a la acción.
- Sección de Vóley (`voley.html`): niveles, horarios, tarifas y galería de imágenes.
- Sección de Contacto (`contacto.html`): formulario para registrar consultas y tabla con los registros capturados.

El diseño mantiene la identidad visual del club (paleta vinculada al escudo), con un layout adaptable a móviles, tabletas y escritorio.

---

## Funcionalidades implementadas

- Formulario de contacto con cinco campos y validaciones:
  - Nombres (requerido, mínimo 3 caracteres)
  - Apellidos (requerido, mínimo 3 caracteres)
  - Correo (tipo email, validado)
  - Teléfono (exactamente 9 dígitos)
  - Mensaje (requerido, mínimo 10 caracteres)

- Validaciones HTML5 y JavaScript para coherencia de datos (filtro en vivo de teléfono y `pattern`).

- Persistencia con LocalStorage: los registros se almacenan en el navegador y permanecen tras recargar.

- Tabla dinámica de registros:
  - Listado con columnas (incluye truncado visual y títulos para ver el contenido completo al pasar el cursor).
  - Búsqueda en vivo por nombre o correo.
  - Eliminación de un registro.
  - Borrar todos los registros.
  - Exportar a JSON los registros guardados.

- Diseño responsivo con CSS Grid y Flexbox, reforzado con utilidades de Bootstrap 5.

---

## Tecnologías utilizadas

- HTML5 semántico: `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`.
- CSS3: estilos personalizados compilados desde `scss/estilos.scss` y `scss/tabla.scss`.
- SASS:
  - Variables (colores, tipografías, sombras)
  - Mixins reutilizables (tarjetas/sombras)
  - Anidación de selectores
- Bootstrap 5 (CDN): tabla, botones y utilidades responsivas.
- JavaScript (Vanilla):
  - Captura y validación del formulario
  - Manipulación del DOM (render dinámico de la tabla)
  - Gestión de eventos
  - Almacenamiento con LocalStorage

---

## Cumplimiento de requisitos

1. HTML5 Semántico  
   Estructura semántica, formulario con 5 campos y tabla con `<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`.

2. CSS3 y diseño responsivo  
   Más de 20 reglas personalizadas, diseño adaptable a distintos dispositivos, uso de Flexbox y CSS Grid.

3. SASS  
   Todo el CSS personalizado proviene de archivos `.scss` (variables, mixins, anidación) compilados a `css/`.

4. Bootstrap 5  
   Integración por CDN y uso de componentes/estilos predefinidos (tabla, botones, rejilla).

5. JavaScript (Vanilla)  
   Captura y validación del formulario, manipulación dinámica del DOM, gestión de eventos, persistencia con LocalStorage, búsqueda, eliminación y exportación.

---

## Ejecución local

Abrir `index.html` (o `contacto.html`) directamente en el navegador. No requiere servidor ni ejecución de comandos.

Nota: para uso sin conexión a Internet, descargar Bootstrap y enlazarlo localmente en lugar del CDN.

---

## Compilación de SASS

Si se modifican los `.scss`, compilar a `css/` con:

```bash (TERMINAL)
npm i -D sass
npx sass scss:css --style=compressed --no-source-map
# o modo observación:
npx sass --watch scss:css --style=compressed --no-source-map
