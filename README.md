# AdExternals

## Descripción / requerimientos

Paquete de apoyo que contiene el software relevante para la utilización de DROID y Jhove en Ubuntu 22.04 o cualquier sistema similar basado en unix que permita la instalación de los siguientes requerimientos:
* Java17, con la siguiente ruta a su binario:
```bash
/usr/lib/jvm/java-17-openjdk-amd64/bin/java
```
* Java21, con la siguiente ruta a su binario:
```bash
/usr/lib/jvm/java-21-openjdk-amd64/bin/java
```
* Como recomendacion, es preferible que el usuario tenga establecida la version de java del sistema de forma manual a la instalacion binaria de Java17 mencionada previamente, y se use la version de Java21 para lanzar DROID de forma manual

## Instalación / setup

Para dejarlo configurado de forma correcta, se recomienda encarecidamente seguir los siguientes pasos, por motivos de configuración y limpieza

1. Abre un terminal y navega hasta tu $HOME (por defecto, nada más abrir un terminal suele estar ya ubicado en dicha ruta):
```bash
cd $HOME
```

2. Copia en el home este mismo repositorio con el comando *git clone*:
```bash
git clone <url: ssh || http>
```

3. Asegurate de que funcionen los comandos para ambas instalaciones. Para comprobar jhove puedes ejecutar lo siguiente tras realizar el paso anterior
```bash
cd AdExternals/jhove_installation/

jhove
```
Si todo ha ido bien, deberías ver una salida como la siguiente, que indique version de jhove, API, configuracion, etc.
```
Jhove (Rel. 1.20.0, 2019-01-19)
 Date: 2025-08-08 18:57:41 CEST
 App:
  API: 1.20.0, 2019-01-19
  Configuration: /etc/jhove/jhove.conf
  JhoveHome: $INSTALL_PATH
  Encoding: utf-8
  TempDirectory: /tmp
  BufferSize: 131072
  Module: AIFF-hul 1.4
  Module: ASCII-hul 1.3
  Module: BYTESTREAM 1.3
  Module: GIF-hul 1.3
  Module: HTML-hul 1.3
  Module: JPEG-hul 1.4
  Module: JPEG2000-hul 1.3
  Module: PDF-hul 1.11
  Module: TIFF-hul 1.8
  Module: UTF8-hul 1.6
  Module: WAVE-hul 1.6
  Module: XML-hul 1.4
  OutputHandler: Audit 1.1
  OutputHandler: TEXT 1.6
  OutputHandler: XML 1.8
  Usage: java JHOVE [-c config] [-m module] [-h handler] [-e encoding] [-H handler] [-o output] [-x saxclass] [-t tempdir] [-b bufsize] [-l loglevel] [[-krs] dir-file-or-uri [...]]
  Rights: Derived from software Copyright 2004-2011 by the President and Fellows of Harvard College. Version 1.7 to 1.11 independently released. Version 1.12 onwards released by Open Preservation Foundation. Released under the GNU Lesser General Public License.
```
4. Para comprobar que funcione bien DROID, vuelve al directorio de AdExternals/ y desde allí navega hasta el directorio que contiene el binario de jhove y su script de interfaz gráfica. Como lo más relevante es el funcionamiento por comando, quedan a continuación los pasos a seguir para probarlo inmediatamente despues del testeo anterior o desde cualquier ruta del sistema
```bash
cd $HOME

cd AdExternals/droid-binary-6.8.1-bin/

chmod +x droid-command-line-6.8.1.jar

/usr/lib/jvm/java-21-openjdk-amd64/bin/java -jar droid-command-line-6.8.1.jar -h
```
