
# Practica 2: Pruebas con gitignore

## 1. Que he probado y como ha funcionado

En esta practica he estado probando como hacer que Git ignore archivos para que no se suban al repositorio, lo he hecho de dos formas:

**Con el archivo global (`~/.gitignore_global`)**
He configurado este archivo en mi carpeta de usuario, le he metido extensiones de archivos que no quiero subir nunca, como `*.o`, `*.log` y `*.zip` ,al crear archivos de prueba con esas extensiones y hacer un `git status`, git los ignoro

**Con el archivo local (`.gitignore`)**
Este lo cree directamente en la carpeta de la practica, aqui probe cosas mas especificas:
* Puse `dir1/*` para ignorar toda la carpeta 1 entera, pero justo debajo puse `!dir1/info.txt` ,el operador `!` sirvio para hacer una excepcion, y al mirar el `git status`, Git me pedia añadir el `info.txt` pero seguia ignorando el resto
* Tambien probe `dir2/*.txt` para ignorar solo los archivos de texto de esa carpeta dejandome subir el `.py`
* Y por ultimo, use `dir3/**/*.txt` para ignorar los textos de la carpeta 3 y tambien de cualquier subcarpeta que tuviera dentro

## 2. Diferencias entre el ignore Global y el Local

Basicamente la diferencia principal que he visto es a quien le afecta:

* **El global:** Afecta a **todos** los repositorios que tengo en mi ordenador, viene genial para poner ahi archivos basura que crea mi propio sistema operativo como `.DS_Store` si usas Mac o cosas de Windows o mi editor de codigo, son cosas mias que al resto del equipo del proyecto no le importan, por eso no se sube
* **El local:** Solo afecta a **este proyecto** en concreto. Este `.gitignore` si que se sube al repositorio para compartirlo con el resto de compañeros aqui es donde se meten las cosas especificas del proyecto que nadie debe subir como carpetas de compilacion o contraseñas de esta aplicacion en concreto

## 3. Capturas de pantalla

![gitignore](<imagen/imagen1.png>)
