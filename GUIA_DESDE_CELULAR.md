# Guía para compilar desde el celular usando GitHub Actions

1. Crea un repositorio en https://github.com/new con el nombre `crucigramas-ilimitados`.
2. Para que GitHub Actions estándar no consuma minutos de compilación privados, puedes marcarlo Public. Ten en cuenta que el código será visible públicamente. No subas contraseñas, claves ni datos personales.
3. Descomprime el ZIP en tu teléfono. Sube al repositorio el CONTENIDO de la carpeta `crucigramas_ilimitados` (incluyendo la carpeta oculta `.github`, `lib`, `pubspec.yaml` y los archivos README). Si la web móvil no deja subir carpetas, usa la opción de cargar archivos desde un navegador en modo escritorio o un cliente Git fiable.
4. Abre la pestaña `Actions` del repositorio y selecciona `Compilar APK Android`.
5. Pulsa `Run workflow` y confirma con el botón verde.
6. Espera que el trabajo termine con marca verde. Abre la ejecución completada y baja hasta `Artifacts`.
7. Descarga `crucigramas-ilimitados-apk-debug`, descomprime el ZIP del artefacto y obtendrás `app-debug.apk`.
8. Abre el APK en tu teléfono. Android podría pedir permiso para instalar aplicaciones desde esa fuente; permite solo para el navegador/gestor que usaste y únicamente si confías en el archivo. Después puedes desactivar el permiso.

Si falla la compilación, abre la ejecución roja, entra en el paso que falló y copia el mensaje de error para revisarlo.

Esta compilación es solo para pruebas. El juego aún no tiene anuncios reales ni suscripciones reales de Google Play; la pantalla Premium es demostrativa. Para publicación comercial habrá que configurar firma de lanzamiento, identificador único, privacidad, pruebas y Google Play Console.
