# Carreteras de Zona 4 Trujillo (Sur-Este) — GitHub Pages

Esta carpeta contiene el visor listo para publicar:

- `index.html` — el mapa completo (carreteras, PK, fondos del IGN, GPS, Referencial/LRS, Wake Lock y coordenadas WGS84/UTM).
- `.nojekyll` — evita que GitHub procese los archivos con Jekyll.

> **Trazas corregidas (18/11/2026):** reconstruidas desde los SHP con tolerancia de 0,5 m
> (antes 30 m, que daba trazas rectas desplazadas). 11.904 vértices, desviación máxima 0,54 m.
> La **CC-429** es la única que difiere de la ortofoto porque su trazado real cambió; el SHP
> procede de mapping mobile y recoge esa modificación. El Referencial se recalibra solo.

El **Referencial/LRS** solo se actualiza al tocar la traza de la carretera (30 m): si haces clic fuera se conserva el último PK mientras buscas coordenadas. Con el GPS activo sigue tu posición.

La **Búsqueda por Referencial** está integrada en la **única caja de búsqueda** (la misma de carreteras y poblaciones): escribe la vía y su PK juntos, p. ej. `CC-420 10+150` o `CC-420 10150` (también `CC-420 10.150`). No hay botón ni panel aparte: el mapa se centra en ese punto (zoom 16) y resalta la carretera y el PK en rojo.

GitHub Pages da **HTTPS gratis**, que es obligatorio para que el GPS funcione en iOS / iPhone.

El propio mapa lleva un botón **Ayuda** en la barra superior con este resumen (PC, GitHub, iOS / iPhone y Android).

---

## Publicar en 5 pasos

1. **Crea cuenta** en https://github.com/signup (si no tienes).

2. **Crea el repositorio**:
   - Pulsa el botón verde **New**.
   - Repository name: `zona4-mapa` (o el nombre que quieras, en minúsculas y sin espacios).
   - Marca **Public** (los repositorios privados no tienen Pages gratis).
   - Opcionalmente marca **Add a README file**.
   - Pulsa **Create repository**.

3. **Sube los archivos**:
   - Dentro del repositorio, pulsa **Add file → Upload files**.
   - Arrastra los 3 archivos: `index.html`, `README.md` y `.nojekyll`.
   - Escribe un mensaje (p. ej. `Publicar mapa Zona 4`) y pulsa **Commit changes**.

4. **Activa Pages**:
   - Ve a **Settings → Pages** (en la pestaña del repositorio).
   - En *Build and deployment*, Source elige **Deploy from a branch**.
   - Branch: **`main`** y carpeta **`/ (root)`**.
   - Pulsa **Save**.

5. **Abre la URL** (espera 1–2 minutos la primera vez):

   ```
   https://TU-USUARIO.github.io/zona4-mapa/
   ```

   Sustituye `TU-USUARIO` por tu nombre de usuario de GitHub y `zona4-mapa` por el nombre del repositorio. **El slash final importa.**

---

## Usarlo en iOS / iPhone

1. Abre **Safari** y pega la URL `https://...` (nunca `http://`): el GPS solo funciona con HTTPS.
2. Pulsa **Activar GPS** y acepta **Permitir** cuando Safari pregunte por la ubicación.
3. Para tenerlo como app: botón **Compartir → Añadir a la pantalla de inicio**. Así se abre siempre en HTTPS y el GPS sigue funcionando.
4. **Pantalla siempre activa:** Safari en iOS no permite Wake Lock. Si se apaga la pantalla, ve a Ajustes → **Pantalla y brillo → Bloqueo automático → Nunca**.

Si no sale el permiso:
- Ajustes → **Privacidad y seguridad → Servicios de ubicación** → activar **Servicios de ubicación** y, dentro de **Safari**, marcar **Precisa**.
- Comprueba que la URL empiece por `https://`.
- Si ves una versión antigua del mapa, cierra la pestaña y vuelve a abrir el enlace.

---

## Usarlo en Android

1. Abre **Chrome** y pega la misma URL `https://...` (nunca `http://`).
2. Pulsa **Activar GPS** y acepta **Permitir**.
3. Para instalarlo: menú de Chrome (**⋮**) → **Añadir a pantalla de inicio** o **Instalar app**. Se abre como una app y siempre usa HTTPS.
4. Si no sale el permiso:
   - Activa la ubicación del móvil en **Ajustes → Ubicación**.
   - **Ajustes → Apps → Chrome → Permisos → Ubicación** → **Solo mientras usas la app** o **Preguntar cada vez**.

Al igual que en el iPhone, el GPS solo funciona con la URL HTTPS de GitHub Pages; abriendo el HTML desde Archivos no hay ubicación.

---

## Controles del mapa

| Control | Función |
|---|---|
| Topográfico / Mapa base / Ortofoto / Sin fondo | Cambia el fondo del IGN |
| Carreteras / PK | Muestra u oculta cada capa |
| Poblaciones | Muestra u oculta los 103 núcleos del IGN (punto azul y etiqueta blanca con borde rojo y texto negro; nombre, habitantes y altitud) |
| Selector de color | Elige el color de las carreteras |
| Selector de grosor | Elige la anchura de las carreteras: **Fino, Medio, Normal, Grueso o Muy grueso** (la carretera seleccionada se resalta) |
| Coordenadas | Muestra/oculta el panel con WGS84 y ETRS89/UTM (huso automático 30N/29N). Dentro tiene dos modos: **Pantalla** (sigue el ratón) y **GPS** (sigue tu ubicación), además de **Copiar** y **Cerrar** |
| Referencial | Recuadro azul con **Vía:** y **PK:** real (p. ej. `1+158 m`). Solo se actualiza al tocar la traza (30 m); si tocas fuera conserva el último PK. Con GPS activo sigue tu posición. Un clic manual tiene prioridad durante 20 s |
| Pantalla siempre activa: OFF/ON | Wake Lock: evita que el móvil apague la pantalla. Si el navegador no lo soporta, muestra aviso con instrucciones para iPhone/iPad |
| Etiquetas carreteras | Muestra u oculta `CC-420`, `CC-432`... (fondo blanco y texto negro; de lejos una por vía y más al acercar) |
| Etiquetas PK | Muestra u oculta `PK-1`, `PK-2`... (fondo amarillo, visibles desde zoom 13) |
| Ver todo | Vuelve a encuadrar la Zona 4 |
| Ayuda | Abre en pantalla el resumen para ordenador, GitHub, iOS / iPhone y Android |
| Buscar (caja única) | Carreteras, PK y poblaciones juntos. Escribe `CC-420 10+150`, `CC-420`, `Trujillo` o `Navezuelas`: con vía + PK va directo al punto (zoom 16) y lo resalta en rojo; con una sola coincidencia va directo; si hay varias (p. ej. `Trujillo`) elige en la lista **Carretera** (→ `CC-330`) o **Población** (→ el pueblo). Flechas y Enter también funcionan |
| Medir distancias | Pulsa el botón, haz clic en el punto de partida y luego en cada punto: muestra el último tramo y la distancia **TOTAL** acumulada |
| Terminar / Borrar | Termina la medición / borra los puntos (panel "Medición") |
| Activar GPS / Desactivar GPS | Activa el GPS; punto azul + círculo de precisión. Con GPS activo, el Referencial calcula el PK de tu vía |
| Siguiendo / Seguir | Reactiva el seguimiento si has arrastrado el mapa |
| Pulsar en el mapa | Muestra **Coordenadas del punto**: WGS84 (lat/lon) y ETRS89 UTM (Este/Norte en metros), con botón **Copiar**. El huso se calcula según la longitud: **30N** en la Zona 4 y **29N** si entra una carretera más al oeste |

Al tocar una carretera ves su longitud en **km** (en negrita), seguida de `/` y los **m** en la misma línea, ambos con el mismo tamaño; la ficha incluye además WGS84 y ETRS89/UTM (huso automático). Al tocar un PK ves su número (sin cota).

También hay una copia ligera (`Mapa_Zona4.html` en la carpeta principal) que
funciona sin internet, y un resumen para ordenador y móvil en `Ayuda.txt`.

---

## Actualizar el mapa más adelante

Sustituye `index.html` por la versión nueva en el repositorio y haz **Commit changes**. GitHub Pages se actualiza solo en 1–2 minutos.

**Nota:** los fondos del IGN se descargan de internet; las carreteras y los PK van dentro del HTML, así que siguen viéndose aunque falle el fondo.
