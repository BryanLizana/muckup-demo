# WireForms · mockup-demo

Editor de wireframes/mockups en **un solo archivo HTML**, sin dependencias ni build.
Se puede usar online (GitHub Pages) o descargado en local, y el mockup se guarda
**dentro del mismo `.html`**.

## Uso

1. Abre la versión online (GitHub Pages) o `index.html` directamente.
2. Arrastra componentes desde la paleta; doble clic para editar texto.
3. Ponle nombre en el campo junto al logo.
4. **💾 Guardar / `Ctrl+S`**
   - **Chrome / Edge:** la primera vez eliges dónde guardar; después `Ctrl+S`
     sobrescribe ese mismo archivo. Al reabrir el `.html` en local y pulsar
     `Ctrl+S`, el navegador pide permiso una vez y lo vuelve a escribir.
   - **Firefox / Safari:** no tienen la API de sistema de archivos, así que
     `Ctrl+S` descarga una copia actualizada.
5. **⬇ Descargar / `Ctrl+Shift+S`**: siempre descarga una copia.
6. **📂 Abrir / `Ctrl+O`**: abre otro mockup `.html` (también los exportados
   con la versión anterior, `window.__WF_INIT__`).

Si cierras sin guardar, el trabajo queda como **borrador** en `localStorage`
y al volver a abrir aparece una barra para *Restaurar* o *Descartar*.

## Cómo funciona el guardado

Los datos viven en un bloque `<script type="application/json" id="wf-data">`.
Al guardar se parte de una copia limpia del documento tomada al arrancar (antes
de renderizar), se reemplaza solo ese bloque y se escribe el archivo. Así el
HTML no se duplica ni crece con cada guardado.

## Publicar en GitHub Pages

Settings → Pages → *Deploy from a branch* → `main` / `(root)`.
