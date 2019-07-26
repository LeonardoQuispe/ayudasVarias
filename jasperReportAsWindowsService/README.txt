-----------------------------------INDICACIONES-----------------------------------------
1. Generar el compilado .jar de tu proyecto Spring Boot (mvn install).
2. Copiar el compilado .jar que se encuentra en la carpeta raiz/target/**.jar
3. Pegarlo dentro de la carpeta JasperService y renombrarlo "gs-serving-web-content.jar"
4. Copiar todo el contenido de esta carpeta en una ubicacion deseada (preferiblemente en la C:/)
   y copiar la URL de la ubicación elegida.
5. Editar el archivo "startJasperReportService.bat" y reemplazar la URL existente con la URL 
   de la ubicacion de su reporte.
6. Ejecutar el archivo "startJasperReportService.bat" y Listo!.. Puedes cambiar el nombre del servicio
   en el mismo archivo "startJasperReportService.bat".





-----------------------------------COMANDOS---------------------------------------------


---------------EXPORTAR ARCHIVO .JAR DE SPRING-BOOT-------------------------------------
mvn install
mvn package && java -jar target/gs-spring-boot-0.1.0.jar (OPCIONAL)



---------------INICIAR API REPORTE A PARTIR DE UN COMPILADO .JAR------------------------
java -jar <jarfilename>.jar


---------------INICIAR API REPORTE DESDE EL PROYECTO SPRING BOOT------------------------
mvn spring-boot:run


---------------CREAR SERVICIO JASPER REPORT---------------------------------------------
sc create JasperReportService binPath= "D:\Escritorio\JASPER\gs-serving-web-content.exe"
sc start JasperReportService
sc delete JasperReportService