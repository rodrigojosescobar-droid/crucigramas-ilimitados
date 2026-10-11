# Crucigramas Ilimitados — MVP Android

Primera versión de prueba hecha en Flutter. Incluye pantalla principal, selección de niveles, crucigrama de muestra, selección de pistas, validación de respuestas, reinicio y pantalla informativa Premium.

## Estado de esta versión
- Funciona localmente sin servidor.
- Incluye contenido de demostración; el banco de palabras es pequeño y debe ampliarse antes del lanzamiento comercial.
- Los anuncios de AdMob y las compras/suscripciones de Google Play NO están conectados. La pantalla Premium es demostrativa y no cobra dinero.
- El tablero es un prototipo visual y debe revisarse/ampliarse junto con el banco de crucigramas para una versión comercial.

## Requisitos
- Flutter SDK estable instalado.
- Android Studio con Android SDK.

## Probar en un teléfono Android
1. Descomprimir el ZIP.
2. Abrir una terminal dentro de la carpeta `crucigramas_ilimitados`.
3. Ejecutar `flutter doctor` y resolver los componentes faltantes.
4. Conectar el teléfono por USB y activar Opciones de desarrollador > Depuración USB.
5. Ejecutar `flutter pub get`.
6. Ejecutar `flutter devices` para verificar que el teléfono aparezca.
7. Ejecutar `flutter run` para instalar y abrir la aplicación en modo de desarrollo.

## Generar APK de prueba
Desde la carpeta del proyecto:

```bash
flutter pub get
flutter build apk --debug
```

El APK de depuración suele quedar en `build/app/outputs/flutter-apk/app-debug.apk`.

## Preparar para Google Play
1. Definir el nombre definitivo y un identificador de paquete único, por ejemplo `com.tumarca.crucigramas`.
2. Crear y proteger la clave de firma de carga.
3. Configurar Google Play App Signing en Play Console.
4. Implementar anuncios reales con el plugin oficial `google_mobile_ads`, usando IDs de prueba durante el desarrollo.
5. Implementar la suscripción anual con Google Play Billing / `in_app_purchase`, validar compras y restauraciones y manejar expiraciones.
6. Añadir política de privacidad, formulario de seguridad de datos, clasificación de contenido, icono, capturas y ficha de tienda.
7. Generar el Android App Bundle: `flutter build appbundle`.
8. Subir primero a prueba interna; después a prueba cerrada y producción, según los requisitos vigentes de Play Console.

## Monetización recomendada
- Gratis: anuncios no intrusivos y acceso inicial limitado o rotación de crucigramas gratuitos.
- Premium anual: todos los niveles, partidas ilimitadas y sin anuncios.
- Precio de prueba de mercado: equivalente local a US$ 9,99/año; definir el precio final en Play Console.

## Antes de publicar
- Revisar las intersecciones del tablero y ampliar a crucigramas completos con muchas palabras.
- Añadir guardado de progreso, estadísticas, dificultad real, más paquetes y desafío diario.
- Probar en varios tamaños de pantalla y con conexión intermitente.
- No publicar como app comercial hasta que anuncios, suscripciones, política de privacidad y banco de contenido estén implementados y probados.
