README - Script de Pruebas de Carga (Login API)

Este repositorio contiene la implementación de una prueba de carga para el servicio de autenticación de FakeStoreAPI.
1. Requisitos del Sistema

Para ejecutar este script, es necesario contar con las siguientes tecnologías:

    Apache JMeter: Versión 5.6.3 (o superior).

    Java JRE/JDK: Versión 17 o superior.

    Sistema Operativo: Independiente (Windows, Linux, macOS).

2. Estructura de Archivos

    ejercicioPerformance.jmx: Script de JMeter con la configuración de la prueba.

    users.csv: Archivo de datos con las credenciales parametrizadas (user, passwd).

    conclusiones.txt: Informe con los hallazgos y resultados de la ejecución.

3. Instrucciones de Ejecución 

    Descarga: Clona este repositorio o descarga todos los archivos en una misma carpeta local.

    Preparación de Datos: Asegúrate de que el archivo users.csv se encuentre en la misma ruta que el archivo .jmx (el script está configurado con una ruta relativa para facilitar su portabilidad).

    Abrir JMeter: Inicia la interfaz gráfica de JMeter (jmeter.bat en Windows o jmeter.sh en Linux).

    Cargar el Script: Ve a File > Open y selecciona el archivo ejercicioPerformance.jmx.

    Ejecución:

        Haz clic en el botón Start (icono de flecha verde) para iniciar la prueba.

        Selecciona el listener Summary Report para visualizar el rendimiento en tiempo real.

    Validación: La prueba se detendrá automáticamente tras completar el ciclo de carga o puedes detenerla manualmente tras observar la estabilidad en los 20 TPS.

4. Configuración de la Prueba

    Escenario: 20 TPS constantes utilizando un Constant Throughput Timer.

    Validaciones:

        El tiempo de respuesta no debe exceder los 1,5 segundos (validado mediante Duration Assertion).

        La tasa de error debe mantenerse por debajo del 3%.
