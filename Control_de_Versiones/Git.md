# Git

## Cómo funciona Git

La mayoría de los otros sistemas almacenan la información como una lista de cambios en los archivos. Estos sistemas manejan la información que almacenan como un conjunto de archivos y las modificaciones hechas a cada uno de ellos a través del tiempo.

| ![Almacenamiento de datos como cambios en una versión de la base de cada archivo](./Funcionamiento_Otros_Sistemas_de_Control_de_Versiones.png) |
|:--:|
| *Almacenamiento de datos como cambios en una versión de la base de cada archivo.* |

Git almacena y maneja la información de forma muy diferente a otros sistemas de control de versiones.

Git maneja sus datos como un conjunto de copias instantáneas, cada vez que se confirma un cambio, Git guarda el estado del proyecto tomando una foto del aspecto de todos los archivos en ese momento y guarda una referencia a esa copia instantánea. Para ser más eficiente si un archivo no se modifica, no almacena de nuevo el archivo, sino un enlace a la ultima versión del archivo que ya tenía almacenado. Y estas copias instantáneas las almacena como una secuencia a través del tiempo.

| ![Almacenamiento de datos como instantáneas del proyecto a través del tiempo](./Funcionamiento_Git.png) |
|:--:|
| *Almacenamiento de datos como instantáneas del proyecto a través del tiempo.* |

La mayoría de operaciones de Git se pueden trabajar de manera local ya que la historia del proyecto se guarda en el disco local.

Para navegar entre la historia del proyecto, Git no requiere conectarse al servidor para obtener la versión y mostrarla, simplemente la lee de la base de datos local del proyecto. Si se quieren comparar los cambios entre dos versiones distintas, Git busca las instantáneas de esos archivos y hace un cálculo de diferencias localmente, en lugar de pedirlo a un servidor remoto.

Esto permite trabajar sin conexión y confirmar cambios libremente y solo subirlos al servidor cuando haya conexión.

## Estado de los archivos en Git

* Untracked: Archivos sin rastrear, son los archivos sobre los que no se tiene un seguimiento en Git, es decir no se tomán en cuanta en la base de datos de Git, son todos los archivos nuevos o ignorados.

* Tracked: Archivos rastreados, son loas archivos sobre los que se tiene seguimiento, para que un archivo nuevo sea rastreado debe cambiar su estado a staged; pueden tener los siguientes estados:
  * Unmodified: Archivos sin modificar, archivos sin modificación después de la última confirmación.
  * **Modified**: Archivos modificados, archivos con algún cambio después de la última confirmación.
  * **Staged**: Archivos preparados, archivos modificados y/o recién rastreados listos para que sus cambios sean confirmados.
  * **Commited**: Archivos confirmados, archivos modificados y/o creados cuyos cambios ya fueron guardados en Git.

Esto nos lleva a las tres secciones principales de un proyecto de Git: El directorio de Git (Git Directory), el directorio de trabajo (Working Directory), y el área de preparación (Staging Area).

| ![Directorio de trabajo, área de almacenamiento y el directorio Git](./Secciones_de_Git.png) |
|:--:|
| *Directorio de trabajo, área de almacenamiento y el directorio Git.* |

* **Working Directory**: Es el area de trabajo, el directorio en el disco donde se encuentran los archivos para que los puedas usar o modificar. Cuando se clona el proyecto desde otra computadora estos archivos se extraen de la base de datos del directorio de Git.

* **Staging Area**: Es el area donde se agregan los archivos modificados que serán enviados en la siguiente confirmación.

* **Git Directory**: Es el directorio de Git donde se almacenan los metadatos y base de datos con la historia del proyecto, este directorio es el que se copia la clonar el repositorio.

## Flujo de trabajo básico en Git

1. Modificas/Agregas/Eliminas una serie de archivos en tu directorio de trabajo.

2. Preparas los archivos, añadiéndolos a tu área de preparación.

3. Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación y almacena esa copia instantánea de manera permanente en tu directorio de Git.
