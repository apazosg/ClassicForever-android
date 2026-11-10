# ClassicForever Android

Aplicación para ejecutar World of Warcraft en dispositivos Android ARM64, con soporte gráfico para Mali/PanVK y Adreno/Turnip y un modo de conexión a Classic Forever.

Este es el repositorio público de **documentación y releases**. Aquí publicaremos los APK que vayamos seleccionando; el código de desarrollo se mantiene en un repositorio privado.

## Descargas

Los APK se publicarán en [Releases](https://github.com/apazosg/ClassicForever-android/releases). **Todavía no hay ninguna versión publicada en este repositorio.**

Cada release indicará los cambios, las instrucciones específicas de esa versión y las limitaciones conocidas. Las publicaciones se realizarán cuando decidamos que una versión está lista para compartir.

## Funcionalidades

- **Instalación del juego desde la aplicación**, con descarga inicial del cliente y descarga progresiva de los datos mientras juegas.
- **Reutilización de una instalación existente**, seleccionando su carpeta o copiando sus archivos desde un ordenador.
- **Actualización del cliente del juego** desde el propio launcher.
- **Soporte gráfico Mali/PanVK y Adreno/Turnip**, según la compatibilidad del dispositivo. No requiere root.
- **Modo Classic Forever y modo oficial**, con configuración y credenciales separadas.
- **Credenciales guardadas**, con contraseñas cifradas mediante Android Keystore y controles para configurarlas, actualizarlas o borrarlas.
- **Selección de región y resolución** de 720p o 1080p.
- **Mandos, controles en pantalla y teclado Android** durante el juego.
- **Superposición de rendimiento y herramientas de diagnóstico** accesibles desde el menú del juego.
- **Consulta del estado público de Classic Forever** y de la versión del cliente instalada.

La presencia de una función no garantiza que todos los dispositivos o versiones del cliente sean compatibles. Consulta los resultados de pruebas más abajo y las notas del APK que instales.

## Requisitos

- Dispositivo **Android ARM64** con GPU y controladores compatibles. En Mali, la compatibilidad depende también del kernel; no basta con tener una GPU Mali.
- Espacio libre suficiente: como referencia, unos **60 GB para los datos del juego**, más aproximadamente **4 GB para la aplicación y su entorno**. El uso inicial es menor y aumenta con la descarga progresiva.
- Conexión a Internet; se recomienda Wi-Fi para las descargas.
- Una cuenta del servidor que vayas a utilizar: **Classic Forever y Battle.net son cuentas distintas**.

## Instalación y primeros pasos

### 1. Instalar la aplicación

Cuando haya una versión disponible, descarga su APK desde [Releases](https://github.com/apazosg/ClassicForever-android/releases) e instálalo en Android. Si el sistema lo solicita, permite instalar aplicaciones desde la aplicación con la que abras el APK.

Las compilaciones actuales pueden aparecer como **WoW Forever Mali**, con el identificador `app.wowforever.mali`.

### 2. Preparar los archivos del juego

Abre la aplicación y concede el permiso de **acceso a todos los archivos** que solicita para gestionar la carpeta del juego.

- **Instalación nueva:** elige la ubicación y pulsa **Download & Install**. La carpeta predeterminada es `/storage/emulated/0/WoW Forever/`. No hace falta descargar todos los datos antes del primer arranque: el cliente los obtiene según los necesita.
- **Instalación existente:** utiliza **Locate Existing Files** para seleccionar su carpeta. Si copias una instalación desde un ordenador, conserva tanto la carpeta `Data/` como el archivo oculto `.build.info` en la raíz de la carpeta del juego.

### 3. Elegir el servidor y configurar el acceso

En la pantalla de configuración, antes de pulsar **Play**:

1. Activa **Classic Forever** si quieres utilizar ese servidor. La opción está desactivada por defecto; desactivada, la aplicación utiliza la ruta oficial.
2. Configura las credenciales del modo seleccionado con **Configure Login** o **Update Login**. Las cuentas guardadas de ambos modos se mantienen separadas.
3. Ajusta la región y la resolución si lo necesitas.
4. Pulsa **Play**. El primer arranque prepara el entorno y puede tardar unos minutos.

#### Acceso a Classic Forever

En las compilaciones actuales, el acceso guardado se envía desde el control flotante **Login CF**:

1. Espera a que aparezca el formulario de acceso del juego.
2. Deja vacíos los campos de cuenta y contraseña, selecciona el campo de cuenta y cierra los diálogos del juego que puedan interferir.
3. Abre **Login CF**, marca la confirmación de esos requisitos y pulsa **Enviar login y escanear**.

La misma acción está disponible en **Menú rápido → Tools**. Si la entrada se interrumpe, vacía de nuevo los campos antes de repetirla.

**Estado actual:** el modo Classic Forever sigue siendo experimental con el cliente actual. Las pruebas registradas no confirman todavía autenticación y entrada al mundo en ese servidor; no debe confundirse un arranque correcto o la pantalla de login con una conexión completada.

### 4. Controles y ajustes durante el juego

- Pulsa **Atrás** para abrir el menú lateral con teclado, controles en pantalla, rendimiento y salida.
- Los mandos utilizan el soporte de gamepad del propio juego.
- Para volver a la configuración cuando la aplicación arranca automáticamente, pulsa Atrás durante la pantalla inicial o mantén **Start + Select + L2 + R2**.
- Los códigos de autenticación adicional, cuando correspondan, se introducen manualmente.

## Dispositivos probados y funcionando

Este registro recoge resultados de esta aplicación. Las pruebas del proyecto original o de otras aplicaciones no se cuentan como confirmación de compatibilidad aquí.

| Dispositivo | Resultado registrado | Detalles | Fecha |
| --- | --- | --- | --- |
| **POCO X8 Pro Max** | **Funcionando según prueba del usuario** | Buen funcionamiento reportado con PanVK 26.3.1 tras corregir un error de validación. No se han registrado la versión exacta del APK, Android, el modo de servidor ni mediciones de rendimiento. | 2026-11-08 |

### Pruebas parciales

| Dispositivo | Entorno | Resultado registrado |
| --- | --- | --- |
| POCO identificado como **xaga** | Mali-G610, Android 14, PanVK 26.3.1 | Arranque, cinemática y pantalla de login con fondo 3D comprobados. Esta prueba no confirma una sesión jugable ni la conexión a Classic Forever. |

Para añadir o actualizar un dispositivo, registraremos **modelo, GPU, versión de Android, versión del APK, modo de servidor, resultado y fecha**. Cuando haya mediciones, incluiremos también resolución, FPS y problemas observados. Los datos que aún no se hayan comprobado quedarán indicados como pendientes, sin dar por compatible un dispositivo únicamente por su GPU.

## Créditos

Proyecto desarrollado de forma independiente, basado originalmente e inspirado en [WoW Forever for Android](https://github.com/jaredgei/wow-forever-android), con trabajo gráfico de referencia de [RealmDeck](https://github.com/apazosg/realmdeck-android).

Proyecto comunitario no oficial, sin afiliación ni respaldo de Blizzard Entertainment. Los APK de esta aplicación no incluyen los archivos del juego de Blizzard.
