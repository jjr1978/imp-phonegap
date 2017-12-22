# README #

Pasos para compilar la aplicacion apk en Android:
1 -- Recordar cambiar numero de Version en config.xml
2 -- cordova build --release android
3 -- Renombrar y copiar en carpeta impuestos-apk el archivo android-release-unsigned.apk del directorio especificado en la salida a impuestos-mrg.apk
4 -- cd a la carpeta impuestos_apk ( cd ../impuestos_apk/)
5 -- jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore impuestos-mrg.jks impuestos-mrg.apk impuestos-mrg (Ingresar pass: apexfp112)
6 -- Renombrar impuestos-mrg.apk a impuestos-mrg_1.apk
7 -- zipalign -v 4 impuestos-mrg_1.apk impuestos-mrg.apk
8 -- Crear una nueva version de la aplicacion en Google Console y subir impuestos-mrg.apk

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