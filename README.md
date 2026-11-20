# ppal_store

Página completa de ppal_store: ropa (sudaderas y camisas), AirPods y perfumes, por mayor y por menor. Negocio en línea de Huehuetenango, Guatemala.

Es **una sola página** (`index.html`) con HTML, CSS y JavaScript juntos. Las fotos ya están dentro del archivo.

## Cómo está organizada

- **Pestañas de productos:** Ropa, AirPods y Perfumes.
- **Dentro de Perfumes:** pestañas Hombres y Mujeres, con los perfumes ordenados por marca. Los unisex aparecen en las dos.
- **Al tocar un producto** se abre su detalle con un botón de WhatsApp que ya lleva escrito el nombre del producto.
- También tiene la animación de AirPods en promoción, el formulario de contacto y el botón redondo de música.

## Archivos

| Archivo | Para qué sirve | ¿Obligatorio? |
|---|---|---|
| `index.html` | La página completa | **Sí** |
| `cancion-1.mp3` y `cancion-2.mp3` | Las dos canciones del botón redondo (suenan una tras otra) | Solo si quieres música |
| `404.html` | Página amable si alguien abre una dirección que no existe | No |
| `README.md` | Esta guía | No |
| `.nojekyll` | Archivo vacío que le dice a GitHub que no procese la página | No (la página funciona sin él) |

Los archivos de música deben estar **en la misma carpeta que `index.html`** y llamarse exactamente así. Si falta alguno, la página funciona igual, solo que sin esa canción.

## Publicar con GitHub Pages (paso a paso)

1. Crea **un solo repositorio** nuevo en GitHub (por ejemplo `ppal_store`) y márcalo como **Public**.
2. Dentro del repositorio, entra a **Add file → Upload files**. Arrastra **los archivos sueltos** (`index.html`, `cancion-1.mp3`, `cancion-2.mp3` y `README.md`), no una carpeta ni el `.zip`. Confirma con **Commit changes**.
3. (Opcional) Para crear `.nojekyll`: **Add file → Create new file**, escribe `.nojekyll` como nombre y confirma con **Commit changes**. No hace falta escribir nada adentro.
4. Ve a **Settings → Pages**.
5. En **Build and deployment**, elige **Deploy from a branch**, rama **main** y carpeta **/ (root)**. Guarda.
6. Espera entre 1 y 10 minutos. Arriba en esa misma pantalla aparecerá la dirección de tu página, con la forma `https://TU-USUARIO.github.io/ppal_store/`.

Para actualizar la página más adelante, sube el nuevo `index.html` con **Add file → Upload files**. Se reemplaza solo.

## Si ves un error 404

**Lo más probable:** el archivo no se llama exactamente `index.html`. Si bajaste varias versiones, el teléfono o la computadora lo pudo renombrar a `index (1).html` o `index (2).html`, y GitHub solo abre la página si el nombre es exacto. En la pantalla principal del repositorio debe verse `index.html`, sin números ni paréntesis. Para corregirlo: abre el archivo en GitHub, toca el lápiz, cambia el nombre a `index.html` y confirma con **Commit changes**.

También revisa:

- `index.html` debe estar en la carpeta principal del repositorio, **no dentro de otra carpeta**. Se ve en la pantalla principal del repositorio, junto a `README.md`.
- No subas el `.zip`: descomprímelo y sube los archivos que trae.
- En **Settings → Pages** debe decir **Deploy from a branch**, rama **main** y carpeta **/ (root)**. Después de guardar, espera hasta 10 minutos.
- El repositorio debe ser **público**. Con una cuenta gratis, GitHub Pages no funciona en repositorios privados.
- Abre la dirección exacta que aparece en **Settings → Pages**. El nombre del repositorio va en la dirección, y las mayúsculas y minúsculas cuentan.
- Si la página abre pero no suena la música: los archivos deben llamarse `cancion-1.mp3` y `cancion-2.mp3` y estar junto a `index.html`. Además, toca la pantalla una vez, porque el navegador no deja sonar el audio antes.

## Contacto

- Instagram: [@ppal_store](https://www.instagram.com/ppal_store?utm_source=ig_web_button_share_sheet&bqrl=ZDNlZDc0MzIxNw==)
- TikTok: [@ppalstorehue](https://www.tiktok.com/@ppalstorehue?is_from_webapp=1&sender_device=pc)
- WhatsApp: [+502 5998 7791](https://wa.me/50259987791) y [+502 4870 3470](https://wa.me/50248703470)

## Formulario de contacto

Usa [FormSubmit](https://formsubmit.co). Envía los mensajes a giancarloggonzalez12@gmail.com con copia a diegojoelpalacios@gmail.com. El teléfono o WhatsApp es obligatorio.

Después de publicar, envía un mensaje de prueba desde el formulario. Llegará un correo de activación a giancarloggonzalez12@gmail.com: ábrelo y confirma (revisa también spam). Hasta que lo confirmes, los mensajes no llegan.

## Cambiar la música

Reemplaza `cancion-1.mp3` o `cancion-2.mp3` por otro mp3 con el mismo nombre. Usa solo música que tengas permiso de usar.

## Agregar o quitar un producto

Cada producto es un bloque `<article class="producto reveal" ...>` dentro de `index.html`. En los perfumes, los datos de la ventana de detalle van en el mismo bloque: `data-presentacion`, `data-perfil`, `data-salida`, `data-corazon` y `data-fondo` (los que estén vacíos no se muestran). Las fotos están al final del archivo, en el listado `IMAGENES`.
