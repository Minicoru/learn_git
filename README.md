# Ejemplos de Git

Este repositorio contiene ejemplos prácticos de comandos básicos de Git. Si eres nuevo en Git o necesitas repasar conceptos clave, este proyecto te ayudará a familiarizarte con las operaciones más comunes.

## Requisitos

Antes de comenzar, asegúrate de tener Git instalado en tu computadora. Puedes descargarlo desde [git-scm.com](https://git-scm.com/).

## Preparacion previa

Es necesario para poder comenzar a trabajar con Git configurar el nombre del usuario y correo electronico el cual este relacionado a los ajustes que se generen para los historiales de Git en la plataforma de versionamiento, como Github, Gitlab, etc...

Para esto es importante ejecutar el comando:

```git config --global user.name "<Nombre_del_usuario>"```

```git config --global user.email <Mail_usuario>```

## Inicializar Repositorio

Para comenzar, genera tu propio repositorio en tu máquina local usando el siguiente comando:

```git init```

## Clonar Repositorio

Tambien puedes generar una copia local de tu proyecto en el repositorio al que quieras colaborar o trabajar, con el siguiente comando:

```git clone <Repositorio_URL>```

## Clonar Repositorio con nombre de carpeta modificado 

Es opcional poder cambiar el nombre de la carpeta destino para el proyecto, por ejemplo con el mismo comando anterior pero agregando un parametro mas al ultimo que seria el nombre de la carpeta destino existente o no sera donde se descargue el repositorio:

```git clone <Repositorio_URL> <Nombre_proyecto_carpeta_alternativo>```

## Agregando ficheros a tu historial de cambios (fotografia actual del control de versiones)

Tambien puedes agregar a tus ficheros de trabajo los archivos que vas generando uno a uno, con el siguiente comando:

```git add <Fichero_local_en_tu_carpeta_de_proyecto>```

## Agregar todos los ficheros actualmente nuevos o modificados

Existe tambien otra forma de agregar los ficheros y es de la siguiente manera:

```git add .```

Con este ejemplo, tomara todos los ficheros localmente dentro de la carpeta raiz en la que estas trabajando y se agregara al listado todos los archivos detectados con cambios.

## Commits, comentando tus ajustes para describir los cambios, mejoras o correcciones efectuadas

Una vez que estes conforme a los ajustes que estas trabajando o realizando, puedes hacer un commit, para generar una fotografia de la version actual de tu proyecto, esto hara que todos los cambios hasta este momento se almacenen en el historico, por lo que es importante tomar en cuenta que todo se guardara siempre y cuando este relacionado al historial de ese commit y esos ajustes.

```git commit -m '<Mensaje_o_comentario_de_los_ajustes_realizados>'```

## Insertando tus ajustes al historial.

Ahora para poder subir a la plataforma los cambios ajustados y agregados al historial, sincronizando el repositorio de forma externa al equipo local de trabajo, se ejecutaria el comando siguiente:

```git push```

## Vincular repositorio local con repositorio externo en plataforma externa como Github, Gitlab o Bitbucket

Para poder ejecutar estas cargas de historiales de cambios o fotografias del proyecto, se debe vincular el proyecto del repositorio destino por ejemplo de Github y contar con los accesos correspondientes otorgados a tu usuario, por ejemplo aplicaria para el caso de que no seas el dueño directo del repositorio en caso contrario si el dueño o propietario es la misma cuenta no deberias tener mayores problemas, pudiendo ejecutar los siguientes comando para vincular el proyecto:

```git remote add origin https://github.com/Minicoru/learn_git.git```

Despues de esto se ejecuta el siguiente comando para hacer el push de la rama local a la rama en la plataforma.

```git push -u origin main```

### Nota:

>Para este punto deberiamos tomar en cuenta que hicimos una conexion con una rama llamada main, para inicializar el proyecto debemos haber partido con una rama llamada ```Master```, sin embargo lo hemos cambiado por ```main``` y para hacer esto se puede hacer uso del siguiente comando:

>```git branch -M main```

## Generar una fotografia rapida del proyecto

Para generar una fotografia hemos visto que los comandos que se deben utilizar son al menos tres, ```git add```, ```git commit -m``` y ```git push```, pero estos se pueden encadenar en la consola de comandos para generar la fotografia y varia por los separadores de los comandos encadenados.

#### MacOS

```git add . && git commit -m "<comentario>" && git push```

#### Windows

```git add . ;; git commit -m "<comentario>" ;; git push```

