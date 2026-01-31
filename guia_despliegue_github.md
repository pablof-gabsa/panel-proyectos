# Guía de Despliegue en GitHub (Remoto)

Como el comando `git` no está disponible directamente en tu terminal actual, la forma más sencilla de subir todo tu nuevo Panel de Proyectos a la web es utilizando **GitHub Desktop** o la **interfaz web**.

Sigue estos pasos para tener tu tablero accesible desde cualquier lugar.

## Paso 1: Preparación en Firebase
Dado que cada proyecto (`01 Santa Isabel`, `02 Barrancas`, etc.) se conecta a su propia base de datos Firebase, necesitas autorizar el dominio donde alojarás tu web (por ejemplo, GitHub Pages).

1.  Ve a la [Consola de Firebase](https://console.firebase.google.com/).
2.  Para **CADA UNO** de tus proyectos (sí, tendrás que hacerlo en todos los que uses):
    *   Ve a **Authentication** > **Settings** (Configuración) > **Authorized Domains** (Dominios autorizados).
    *   Haz clic en "Add Domain" (Agregar dominio).
    *   Escribe: `tousuario.github.io` (reemplaza 'tousuario' con tu nombre de usuario de GitHub).
    *   Esto es crucial; si no lo haces, la base de datos bloqueará el acceso desde la nueva web.

## Paso 2: Subir el Código a GitHub

### Opción A: Usando GitHub Desktop (Recomendada)
1.  Descarga e instala [GitHub Desktop](https://desktop.github.com/).
2.  Abre la aplicación e inicia sesión con tu cuenta de GitHub.
3.  Ve a **File** > **Add Local Repository**.
4.  Selecciona la carpeta principal: `c:\Users\pablo\Desktop\pablo\check list de tareas interactivo`.
5.  Te dirá que "This directory does not appear to be a Git repository". Haz clic en **Create a Repository here**.
6.  Ponle un nombre (ej: `panel-proyectos`).
7.  Haz clic en **Create Repository**.
8.  Haz clic en **Publish repository** (botón azul arriba).
    *   Asegúrate de **desmarcar** la casilla "Keep this code private" si quieres usar GitHub Pages gratis (o déjala marcada si tienes GitHub Pro).
9.  Pulsa **Publish Repository**.

### Opción B: Usando la Web de GitHub (Manual)
1.  Crea un [Nuevo Repositorio](https://github.com/new). Llámalo `panel-proyectos`.
2.  En la página de configuración, selecciona "Public".
3.  Una vez creado, verás la opción de "uploading an existing file".
4.  Arrastra **TODO** el contenido de tu carpeta `check list de tareas interactivo` (incluyendo `index.html` y todas las carpetas `00...`, `01...`) al área de carga.
5.  Espera a que suban todos los archivos y haz clic en **Commit changes**.

## Paso 3: Activar GitHub Pages
Una vez que tu código esté subido:

1.  Ve a la pestaña **Settings** (Configuración) de tu nuevo repositorio en GitHub.
2.  En el menú lateral izquierdo, haz clic en **Pages**.
3.  En "Build and deployment" > "Branch", selecciona `main` (o `master`) y la carpeta `/(root)`.
4.  Haz clic en **Save**.
5.  Espera unos minutos (1-3 min). Refresca la página y verás un mensaje: *"Your site is live at..."*.

¡Esa será tu nueva URL pública! Podrás entrar desde el móvil o cualquier PC.

## Resumen de Cambios Recientes
Tu panel local ya está optimizado para esto:
-   **Navegación**: El botón "Volver al Panel" funcionará perfectamente en la web.
-   **Modo Admin**: Tu configuración de proyectos ocultos/visibles se guardará en cada navegador que uses (se guarda localmente en el dispositivo).
