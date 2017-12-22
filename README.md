# README #

Pasos para compilar la aplicacion apk en Android:
* Recordar cambiar numero de Version en config.xml
* cordova build --release android
* Renombrar y copiar en carpeta impuestos-apk el archivo android-release-unsigned.apk del directorio especificado en la salida a impuestos-mrg.apk
* cd a la carpeta impuestos_apk ( cd ../impuestos_apk/)
* jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore impuestos-mrg.jks impuestos-mrg.apk impuestos-mrg (Ingresar pass: apexfp112)
* Renombrar impuestos-mrg.apk a impuestos-mrg_1.apk
* zipalign -v 4 impuestos-mrg_1.apk impuestos-mrg.apk
* Crear una nueva version de la aplicacion en Google Console y subir impuestos-mrg.apk

### What is this repository for? ###

* Quick summary
* Version
* [Learn Markdown](https://bitbucket.org/tutorials/markdowndemo)

### How do I get set up? ###

* Summary of set up
* Configuration
* Dependencies
* Database configuration
* How to run tests
* Deployment instructions

### Contribution guidelines ###

* Writing tests
* Code review
* Other guidelines

### Who do I talk to? ###

* Repo owner or admin
* Other community or team contact