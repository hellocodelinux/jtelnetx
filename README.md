# JTelnetX - DX Cluster Hunter

**JTelnetX** es un cliente Telnet especializado, desarrollado en Java, diseñado para radioaficionados (HAM) que disfrutan de la "caza" de comunicados a larga distancia (DX). El programa se conecta a servidores de DX Cluster para monitorear en tiempo real los "spots" (reportes de estaciones activas) y ofrece herramientas para identificar rápidamente las estaciones que son de interés.

Creado por **Eduardo Castillo (LU9DCE)**.

---

## Características Principales

*   **Conexión a DX Cluster**: Conéctate a tu DX Cluster preferido a través de Telnet simplemente ingresando la IP y el puerto.
*   **Interfaz de Terminal Clásica**: Una interfaz limpia y sencilla estilo terminal, con texto coloreado para una fácil lectura de los spots.
*   **Resaltado de Spots**: Los spots se resaltan automáticamente con diferentes colores según el modo de operación (CQ/DX, Digital, CW), permitiéndote identificar rápidamente lo que buscas.
*   **Integración con Log ADI**: Carga tu archivo de log en formato `.adi` para que el programa pueda verificar si un spot corresponde a una estación que ya has contactado.
*   **Alertas para Nuevos Contactos**:
    *   **Alerta Visual**: Muestra una notificación emergente en pantalla cuando aparece un spot de una estación que no está en tu log.
    *   **Alerta Sonora**: Emite un sonido de alerta para los nuevos posibles contactos.
*   **Control de RBN (Reverse Beacon Network)**: Activa o desactiva fácilmente la recepción de spots de skimmers de la RBN.
*   **Función de AutoSpot**:
    *   El programa puede escuchar en puertos TCP (52001) y UDP (2333) para recibir datos en formato ADIF de otros programas (como WSJT-X, JTDX, etc.).
    *   Cuando recibe un nuevo contacto, lo formatea y lo envía automáticamente como un spot al DX Cluster conectado.
*   **Guardado de Configuración**: Guarda tu indicativo (licencia), la dirección del cluster y la ruta de tu archivo ADI para no tener que configurarlo todo cada vez que inicias el programa.
*   **Multiplataforma**: Al estar hecho en Java, puede ejecutarse en Windows, macOS y Linux, siempre que tengas el JRE (Java Runtime Environment) instalado.

---

## ¿Cómo Empezar?

1.  **Configuración Inicial**:
    *   Ve al menú `CONFIGURACION` -> `CLUSTER` -> `USUARIO` para ingresar tu indicativo (callsign/licencia).
    *   Luego, en `CONFIGURACION` -> `CLUSTER` -> `URL IP` para definir la dirección y puerto de tu cluster preferido (ej: `dxc.ve7cc.net:23`).

2.  **Cargar tu Log (Opcional pero recomendado)**:
    *   Para aprovechar las alertas de nuevos contactos, ve a `CONFIGURACION` -> `ADI` -> `CARGAR ADI`.
    *   Selecciona tu archivo de log con extensión `.adi`. El botón "ADI" en la parte inferior se pondrá verde para indicar que se ha cargado correctamente.

3.  **Guardar la Configuración**:
    *   Una vez configurado tu indicativo y cluster, ve a `ARCHIVO` -> `GUARDAR` para que el programa recuerde tus datos la próxima vez que lo abras.

4.  **Conectar**:
    *   Haz clic en `ARCHIVO` -> `CONECTAR`. El programa se conectará al cluster y comenzará a mostrar los spots. El botón "ONLINE" se pondrá verde.

5.  **Activar Alertas y AutoSpot**:
    *   En el menú `ALERTA`, puedes activar las notificaciones `SONIDO` y/o `VISUAL`.
    *   En el menú `AUTOSPOT`, puedes activar los listeners `TCP` o `UDP` para que JTelnetX reciba datos de tu software de logging y pueda enviar spots automáticamente.

---

## Ejecución

Ejecutar el programa necesitarás tener Java instalado.

1.  Abre una terminal o línea de comandos en el directorio donde se encuentra el archivo.

2.  Ejecuta el programa:
    ```bash
    java jtelnetx
    ```

---

## Dependencias

El programa utiliza únicamente las librerías estándar de Java (Swing, AWT, IO, Net), por lo que no requiere dependencias externas.

---

73 y buenos DX!
