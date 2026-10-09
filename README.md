# Tablero Meta Ads — Mar Azul Suites

Seguimiento semanal de las campañas de Meta Ads para el equipo. Espejo del pickup de
ocupación (`ocupacion-marazul`): sitio estático en GitHub Pages con los datos cifrados.

URL del equipo: https://agustinalvarezspj.github.io/ads-marazul/

## Cómo funciona

- `index.html` — el tablero, con la pantalla de acceso. No tiene ningún dato adentro.
- `datos.json` — los cortes publicados, **cifrados**. Es lo único que cambia semana a semana.
- `publicar.bat` / `publicar.ps1` — sube el `datos.json` nuevo al repo (si no usás token).
- `robots.txt` — mantiene el sitio fuera de los buscadores.
- `README-SEGURIDAD.md` — leelo antes de crear tu contraseña.

Fuera del repo (en `.gitignore`, solo en la compu del administrador):

- `semilla-ads.js` / `semilla-ads.json` — los cortes en claro. **Nunca se suben.**

## Qué muestra

- **Acumulado del mes**: los números tal cual salen de Meta a la fecha de corte.
- **El período**: lo que sumó el tramo (acumulado de hoy − corte anterior del mismo mes),
  con flechas contra el **ritmo diario** del período anterior.
- Costo por conversación, volumen y CTR por campaña; tabla con columnas de período
  (marca campañas *nuevas* y *pausadas*); análisis de Claude por corte.
- **Evolución**: mes a mes y gráficos corte a corte.

## Primer acceso (una sola vez)

1. Doble clic en `index.html` **desde esta carpeta** (no desde la URL).
2. "Primer acceso" → crear usuario con una frase larga (12+, ideal 4-5 palabras).
   Anotala antes en el gestor de contraseñas: no hay recuperación.
3. Si `semilla-ads.js` está en la carpeta, los cortes históricos entran solos.
   Si no, botón **Importar** → `semilla-ads.json`.
4. **Publicar cambios** → descarga `datos-ads.json` cifrado → doble clic en `publicar.bat`.
5. En la URL publicada: **Equipo** → alta de cada persona → Publicar de nuevo.
6. Opcional: **Equipo → Publicación directa** → pegar un token fine-grained
   (solo repo `ads-marazul`, permiso *Contents: Read and write*). Desde ahí
   "Publicar cambios" sube directo, sin el bat.

## Rutina semanal

1. URL del tablero → login → **+ Nuevo corte**: nombre, fecha, reservas, facturación.
2. Pegar las filas de campañas directo desde Sheets (sin encabezados, Ctrl+V).
   Orden: campaña · conversaciones · presupuesto · costo x conv · alcance · impresiones · frecuencia · CTR.
3. Pegar el análisis de Claude en su campo.
4. **Publicar cambios**.

## Ojo con esto

- Cargá siempre desde la misma computadora y navegador: el borrador vive ahí.
  "Descartar borrador" vuelve a lo publicado.
- Exportá el CSV cada tanto como respaldo en claro, y guardalo fuera de esta carpeta.
- Nunca subas al repo nada sin cifrar. `publicar.ps1` tiene freno, pero igual.
