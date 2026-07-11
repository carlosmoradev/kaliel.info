# Kaliel Angelical - Landing Page

Sitio web estático creado para Kaliel Angelical. Está construido con **HTML5 puro** y **Tailwind CSS** (vía CDN para máxima simplicidad de despliegue).

## Estructura del Proyecto

- `index.html`: Archivo principal que contiene toda la estructura, diseño (Tailwind) y contenido.
- `.gitignore`: Configuración base de git.

## Cómo desplegar en GitHub Pages

Al usar HTML y Tailwind por CDN, no necesitas configurar ningún proceso de compilación complejo (como Node.js, Webpack o Vite). El despliegue es inmediato:

1. Subí este código a un repositorio público (o privado, dependiendo de tu plan) en tu cuenta de GitHub.
2. En GitHub, andá a la pestaña **Settings** del repositorio.
3. En el menú lateral izquierdo, hacé clic en **Pages**.
4. En **Source**, seleccioná la rama `main` (o `master`) y la carpeta `/ (root)`.
5. Hacé clic en **Save**.

En unos minutos, el sitio estará disponible en `https://<tu-usuario>.github.io/<tu-repositorio>`.

## Configuración del Dominio (kaliel.info)

Para que el dominio `kaliel.info` funcione correctamente con GitHub Pages, debés configurar los DNS en el panel de tu proveedor de dominio (Godaddy, Namecheap, Hostinger, etc):

1. **Récords A (Para el dominio raíz `kaliel.info`):**
   Creá 4 récords tipo `A` con host/nombre `@` apuntando a las siguientes IPs de GitHub:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`

2. **Récord CNAME (Para el subdominio `www`):**
   Creá un récord tipo `CNAME` con host/nombre `www` apuntando a tu usuario de GitHub:
   - `carlosmoradev.github.io`

*Nota: El archivo `CNAME` incluido en este repositorio le avisa automáticamente a GitHub Pages que querés usar este dominio.*

Para que el sitio esté 100% listo, debes editar el archivo `index.html` y actualizar lo siguiente:

1. **Foto de Perfil:** Buscá la etiqueta `<div class="absolute inset-0...` en la sección "Sobre Mí" y reemplazala por una etiqueta `<img>` con la foto real de Kaliel.
2. **Enlaces de Contacto:**
   - Reemplazá el número de teléfono `5491100000000` en el enlace de WhatsApp por el número real.
   - Reemplazá el enlace `https://instagram.com/kalielangelical` por el usuario real de Instagram.
3. **Textos:** Revisá los textos genéricos (X años, historias) y ajustalos con la biografía real.

## Personalización de Colores

Los colores están definidos en la sección `<script>` del `head` en `index.html`. Podés ajustar los tonos de la paleta oficial (violeta, dorado, crema) cambiando los valores hexadecimales dentro del objeto `kaliel`.
