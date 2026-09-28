# ReadyStroke Caddie — piloto visual 0.1

Interfaz de demostración para la app de pruebas RS. La única página es `index.html`; contiene sus estilos, lógica y un logotipo provisional de ReadyStroke en el mismo archivo.

## Configuración por club

Al principio del bloque `<script>` de `index.html`:

```js
const CONFIG = {clubName: 'Meaztegi Golf', clubLogoUrl: ''};
```

- `clubName`: nombre del club mostrado en la introducción.
- `clubLogoUrl`: URL HTTPS del logotipo del club. Mientras esté vacía, se muestra el perfil dorado provisional de ReadyStroke. Si falla la carga del logo, vuelve a ese perfil.
- El nombre del producto permanece **ReadyStroke Caddie** para todos los clubes.
- ES/EN se escoge según el idioma del dispositivo. Los textos ingleses siguen inglés británico.

## Publicación de prueba con GitHub Pages

1. Crear un repositorio para este piloto, por ejemplo `readystroke-caddie-demo`.
2. Subir `index.html` a la raíz de la rama `main`.
3. En **Settings → Pages → Build and deployment**, seleccionar **Deploy from a branch**, rama `main`, carpeta `/(root)` y **Save**.
4. Esperar a que GitHub muestre la URL HTTPS de Pages y abrirla en un móvil.
5. En la app de pruebas RS, pestaña oculta **CADDIE**, añadir **Web Embed** con esa URL. Seleccionar el mayor tamaño adecuado y permitir el scroll del embed. Quitar el texto provisional si se duplicase.
6. Comprobar en el móvil la entrada desde MAP, HOLES, GREENS y CLUB, el envío de una pregunta de prueba, el teclado, el scroll de los mensajes y el botón Atrás que vuelve al mismo hoyo o green.

## Límite actual

Las respuestas son un texto de demostración. No hay conexión con RS Management, API, almacenamiento de preguntas ni generación de respuestas. No se incluye ninguna clave de API en esta página estática. Antes de conectar el backend se definirán fuente aprobada, vigencia, destinatarios, privacidad, costes y la información de contexto que llega desde cada sección.
