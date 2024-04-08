# Ejemplos de Git

Este repositorio contiene ejemplos prácticos de comandos básicos de Git. Si eres nuevo en Git o necesitas repasar conceptos clave, este proyecto te ayudará a familiarizarte con las operaciones más comunes.

## Requisitos

Antes de comenzar, asegúrate de tener Git instalado en tu computadora. Puedes descargarlo desde [git-scm.com](https://git-scm.com/).

## Preparacion previa

Es necesario para poder comenzar a trabajar con Git configurar el nombre del usuario y correo electronico el cual este relacionado a los ajustes que se generen para los historiales de Git en la plataforma de versionamiento, como Github, Gitlab, etc...

Para esto es importante ejecutar el comando:

```
git config --global user.name "<Nombre_del_usuario>"
git config --global user.email <Mail_usuario>
```

## Inicializar Repositorio

Para comenzar, genera tu propio repositorio en tu máquina local usando el siguiente comando:

```
git init
```

## Clonar Repositorio

Tambien puedes generar una copia local de tu proyecto en el repositorio al que quieras colaborar o trabajar, con el siguiente comando:

```
git clone <Repositorio_URL>
```

## Clonar Repositorio con nombre de carpeta modificado 

Es opcional poder cambiar el nombre de la carpeta destino para el proyecto, por ejemplo con el mismo comando anterior pero agregando un parametro mas al ultimo que seria el nombre de la carpeta destino existente o no sera donde se descargue el repositorio:

```
git clone <Repositorio_URL> <Nombre_proyecto_carpeta_alternativo>
```

## Agregando ficheros a tu historial de cambios (fotografia actual del control de versiones)

Tambien puedes agregar a tus ficheros de trabajo los archivos que vas generando uno a uno, con el siguiente comando:

```
git add <Fichero_local_en_tu_carpeta_de_proyecto>
```

## Agregar todos los ficheros actualmente nuevos o modificados

Existe tambien otra forma de agregar los ficheros y es de la siguiente manera:

```
git add .
```

Con este ejemplo, tomara todos los ficheros localmente dentro de la carpeta raiz en la que estas trabajando y se agregara al listado todos los archivos detectados con cambios.

## Commits, comentando tus ajustes para describir los cambios, mejoras o correcciones efectuadas

Una vez que estes conforme a los ajustes que estas trabajando o realizando, puedes hacer un commit, para generar una fotografia de la version actual de tu proyecto, esto hara que todos los cambios hasta este momento se almacenen en el historico, por lo que es importante tomar en cuenta que todo se guardara siempre y cuando este relacionado al historial de ese commit y esos ajustes.

```
git commit -m '<Mensaje_o_comentario_de_los_ajustes_realizados>'
```

## Insertando tus ajustes al historial.

Ahora para poder subir a la plataforma los cambios ajustados y agregados al historial, sincronizando el repositorio de forma externa al equipo local de trabajo, se ejecutaria el comando siguiente:

```
git push
```

## Vincular repositorio local con repositorio externo en plataforma externa como Github, Gitlab o Bitbucket

Para poder ejecutar estas cargas de historiales de cambios o fotografias del proyecto, se debe vincular el proyecto del repositorio destino por ejemplo de Github y contar con los accesos correspondientes otorgados a tu usuario, por ejemplo aplicaria para el caso de que no seas el dueño directo del repositorio en caso contrario si el dueño o propietario es la misma cuenta no deberias tener mayores problemas, pudiendo ejecutar los siguientes comando para vincular el proyecto:

```
git remote add origin https://github.com/Minicoru/learn_git.git
```

Despues de esto se ejecuta el siguiente comando para hacer el push de la rama local a la rama en la plataforma.

```
git push -u origin main
```

### Nota:

> Para este punto deberiamos tomar en cuenta que hicimos una conexion con una rama llamada main, para inicializar el proyecto debemos haber partido con una rama llamada ```Master```, sin embargo lo hemos cambiado por ```main``` y para hacer esto se puede hacer uso del siguiente comando:

```
git branch -M main
```

## Generar una fotografia rapida del proyecto

Para generar una fotografia hemos visto que los comandos que se deben utilizar son al menos tres, ```git add```, ```git commit -m``` y ```git push```, pero estos se pueden encadenar en la consola de comandos para generar la fotografia y varia por los separadores de los comandos encadenados.

### Ejemplos

#### MacOS

```
git add . && git commit -m "<comentario>" && git push
```

#### Windows

```
git add . ;; git commit -m "<comentario>" ;; git push
```

## Estado de los cambios efectuados

Tambien existe el parametro ```status``` que te indicara cuales son los ficheros modificados e insertados como nuevos al repositorio de tu proyecto actualmente durante la edicion de la instancia de tu proyecto, llamandose de la siguiente forma:

```
git status
```

## Historial de fotografias del repositorio

Para obtener el historial de las fotografias (versionamiento del proyecto en ajustes), se llama a ```log``` y este lanzara un listado de los detalles, comentarios, fecha, hora y autor quien realizo las modificaciones al proyecto.

```
git log
```

Dejo un ejemplo de lo que obtengo yo al estar escribiendo y ajustando este ```README.md```

```
commit 6304e6478855aac1a6c1c2e6b329abc08379fa10 (HEAD -> main, origin/main)
Author: Minicoru <miarg49@gmail.com>
Date:   Mon Apr 8 00:34:05 2024 -0400

    Ajustando el readme de este tutorial simple.

commit 12f26c3dfa3b283a33f91f53c774ac3baca3f631
Author: Minicoru <miarg49@gmail.com>
Date:   Mon Apr 8 00:32:16 2024 -0400

    Ajustando el readme de este tutorial simple.

commit 948ae7b12e498a541a66297762bc64d90ede1e17
Author: Minicoru <miarg49@gmail.com>
Date:   Mon Apr 8 00:29:51 2024 -0400

    Ajustando el readme de este tutorial simple.

commit ae65eff584ba369bd142e87015e2036ef28a8720
Author: Minicoru <miarg49@gmail.com>
Date:   Mon Apr 8 00:28:29 2024 -0400

    Ajustando el readme de este tutorial simple.

commit 7fc8d350072386e3dfeaf492a5adbaeb810fa662
Author: Minicoru <miarg49@gmail.com>
Date:   Mon Apr 8 00:26:51 2024 -0400

    Ajustando el readme de este tutorial simple.

commit 71dfcdea1ef5572bf3d2ec70313855601b45aba3
Author: Minicoru <miarg49@gmail.com>
Date:   Mon Apr 8 00:24:48 2024 -0400

    Ajustando el readme de este tutorial simple.

commit f6a3b857dddc54e685cc43e3727088b56266df2b
Author: Minicoru <miarg49@gmail.com>
Date:   Mon Apr 8 00:20:24 2024 -0400

    Ajustando el readme de este tutorial simple.
```