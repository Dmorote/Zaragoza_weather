 # 🌤️ Zaragoza Weather – Widget del tiempo con AEMET

Widget visual del tiempo para **Zaragoza (ES)**, construido con **HTML, CSS y JavaScript**, que consume la API oficial de **AEMET OpenData** y se puede usar como pseudo‑app en el iPhone añadiéndolo a la pantalla de inicio.

Demo (GitHub Pages):  
➡️ [https://dmorote.github.io/Zaragoza_weather/](https://dmorote.github.io/Zaragoza_weather/)

---

## ✨ Características

- 🔗 **Datos oficiales de AEMET** (OpenData, predicción diaria por municipio).
- 🏙️ **Escena isométrica de Zaragoza** que cambia según el tiempo:
  - Despejado
  - Nublado
  - Lluvia
  - Nieve
  - Tormenta
  - Niebla
- 🌈 **Diseño tipo widget / app móvil**:
  - Tarjeta limpia y moderna
  - Iconos, temperatura y descripción centrados
  - Tira de *forecast* de los próximos días en la parte inferior
- ⚡ **Rendimiento optimizado**:
  - Cache en `localStorage` (evita llamar a AEMET en cada carga)
  - Actualización automática cada 30 minutos
  - Botón de **Actualizar** manual
- 🧱 100% **frontend**: solo necesitas un navegador (no hay backend).

---

## 🧩 Tecnologías utilizadas

- **HTML5**
- **CSS3** (diseño responsive y efectos visuales)
- **JavaScript** (fetch API + lógica de negocio)
- **AEMET OpenData**:  
  - Documentación oficial: [https://opendata.aemet.es](https://opendata.aemet.es)

---

## 🛰️ Fuente de datos: AEMET OpenData

Este proyecto utiliza la API de AEMET para obtener la **predicción diaria por municipio**:

- Endpoint metadatos:
  `https://opendata.aemet.es/opendata/api/prediccion/especifica/municipio/diaria/{idMunicipio}/?api_key=TU_API_KEY`
- Luego, con la URL del campo `datos`, se hace una segunda petición para descargar el JSON de predicción.

En este caso se usa el ID de municipio de **Zaragoza**:

- `ZARAGOZA_ID = '50297'`

Más info en la documentación oficial de AEMET.

---

## 🔑 Configuración de la clave de AEMET

Para usar tu propia clave:

1. Regístrate en AEMET OpenData y obtén tu API key (JWT).
2. En el archivo `index.html`, localiza esta línea en el `<script>`:

   ```js
   const AEMET_API_KEY = 'TU_API_KEY_AQUI';

## 📝 Licencia
Este proyecto es solo para fines personales y educativos.
