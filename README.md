# Ejemplos de Git

Este repositorio contiene ejemplos prácticos de comandos básicos de Git. Si eres nuevo en Git o necesitas repasar conceptos clave, este proyecto te ayudará a familiarizarte con las operaciones más comunes.

## Requisitos

Antes de comenzar, asegúrate de tener Git instalado en tu computadora. Puedes descargarlo desde [git-scm.com](https://git-scm.com/).

## Clonar este Repositorio

Es necesario para poder comenzar a trabajar con Git configurar el nombre del usuario y correo electronico el cual este relacionado a los ajustes que se generen para los historiales de Git en la plataforma de versionamiento, como Github, Gitlab, etc...

Para esto es importante ejecutar el comando:

```git config --global user.name "<Nombre_del_usuario>"```
```git config --global user.email <Mail_usuario>```

## Clonar este Repositorio

Para comenzar, genera tu propio repositorio en tu máquina local usando el siguiente comando:

```git init```

O tambien puedes generar una copia local de tu proyecto en el repositorio al que quieras colaborar o trabajar, con el siguiente comando:

```git clone <Repositorio_URL>```

Es opcional poder cambiar el nombre de la carpeta destino para el proyecto, por ejemplo con el mismo comando anterior pero agregando un parametro mas al ultimo que seria el nombre de la carpeta destino existente o no sera donde se descargue el repositorio:

```git clone <Repositorio_URL> <Nombre_proyecto_carpeta_alternativo>```

Tambien puedes agregar a tus ficheros de trabajo los archivos que vas generando uno a uno, con el siguiente comando:

```git add <Fichero_local_en_tu_carpeta_de_proyecto>```

Existe tambien otra forma de agregar los ficheros y es de la siguiente manera:

```git add .```

Con este ejemplo, tomara todos los ficheros localmente dentro de la carpeta raiz en la que estas trabajando y se agregara al listado todos los archivos detectados con cambios.

Una vez que estes conforme a los ajustes que estas trabajando o realizando, puedes hacer un commit, para generar una fotografia de la version actual de tu proyecto, esto hara que todos los cambios hasta este momento se almacenen en el historico, por lo que es importante tomar en cuenta que todo se guardara siempre y cuando este relacionado al historial de ese commit y esos ajustes.

```git commit -m '<Mensaje_o_comentario_de_los_ajustes_realizados>'```

Ahora para poder subir a la plataforma los cambios ajustados y agregados al historial, sincronizando el repositorio de forma externa al equipo local de trabajo, se ejecutaria el comando siguiente:

```git push```

Para poder ejecutar estas cargas de historiales de cambios o fotografias del proyecto, se debe vincular el proyecto del repositorio destino por ejemplo de Github y contar con los accesos correspondientes otorgados a tu usuario, por ejemplo aplicaria para el caso de que no seas el dueño directo del repositorio en caso contrario si el dueño o propietario es la misma cuenta no deberias tener mayores problemas, pudiendo ejecutar los siguientes comando para vincular el proyecto:

```git 