# Práctica de Git: Tutorial basado en Pro Git

**Actividad 2 – Hands on: configuración de herramientas**
Curso: Ciencia de Datos Profesional · Autor: Ricardo (trabajo individual)
Universidad: Fundación Universitaria Agraria de Colombia (UNIAGRARIA)

Este repositorio contiene un tutorial de Git elaborado a partir del libro oficial
[Pro Git (2.ª edición, en español)](https://git-scm.com/book/es/v2) de Scott Chacon y Ben Straub.
Cada uno de los 10 capítulos del libro se resumió en un documento de Word independiente y se exportó a PDF.
Todo el proceso se hizo con comandos básicos de Git y mensajes de commit descriptivos.

## Estructura del repositorio

```
Practica-ciencia-datos-practica-2/
├── README.md
└── docs/
    ├── 01-inicio-control-de-versiones.docx / .pdf
    ├── 02-fundamentos-de-git.docx / .pdf
    ├── 03-ramificaciones-en-git.docx / .pdf
    ├── 04-git-en-el-servidor.docx / .pdf
    ├── 05-git-en-entornos-distribuidos.docx / .pdf
    ├── 06-github.docx / .pdf
    ├── 07-herramientas-de-git.docx / .pdf
    ├── 08-personalizacion-de-git.docx / .pdf
    ├── 09-git-y-otros-sistemas.docx / .pdf
    └── 10-los-entresijos-internos-de-git.docx / .pdf
```

|N.º|Capítulo de Pro Git|Documento|
|-|-|-|
|1|Inicio - Sobre el Control de Versiones|`docs/01-inicio-control-de-versiones`|
|2|Fundamentos de Git|`docs/02-fundamentos-de-git`|
|3|Ramificaciones en Git|`docs/03-ramificaciones-en-git`|
|4|Git en el Servidor|`docs/04-git-en-el-servidor`|
|5|Git en entornos distribuidos|`docs/05-git-en-entornos-distribuidos`|
|6|GitHub|`docs/06-github`|
|7|Herramientas de Git|`docs/07-herramientas-de-git`|
|8|Personalización de Git|`docs/08-personalizacion-de-git`|
|9|Git y Otros Sistemas|`docs/09-git-y-otros-sistemas`|
|10|Los entresijos internos de Git|`docs/10-los-entresijos-internos-de-git`|

## Proceso seguido (paso a paso)

### 1\. Cuenta de GitHub

Registro en [https://github.com](https://github.com) y configuración de acceso (SSH o Personal Access Token).

### 2\. Instalación y configuración de Git

```bash
git --version
git config --global user.name "Ricardo"
git config --global user.email "correo@ejemplo.com"
git config --global init.defaultBranch main
git config --list
```

### 3\. Creación del repositorio en GitHub

En GitHub: **New repository** → nombre `Practica-ciencia-datos-practica-2` → sin README inicial → **Create repository**.

### 4\. Clonación del repositorio

```bash
git clone https://github.com/requiempax/Practica-ciencia-datos-practica-2.git
cd Practica-ciencia-datos-practica-2
```

### 5\. Elaboración de los documentos

Se redactó un documento de Word por capítulo (consultando Pro Git) y luego se exportó cada uno a PDF
(*Archivo → Exportar → Crear documento PDF/XPS*). Los archivos se guardaron en la carpeta `docs/`.

### 6\. Ciclo add → commit → push por capítulo

Al terminar cada capítulo se repitió el mismo ciclo. Ejemplo con el capítulo 1:

```bash
git status
git add docs/01-inicio-control-de-versiones.docx docs/01-inicio-control-de-versiones.pdf
git commit -m "Agrega capítulo 1 (Inicio) del tutorial de Git en Word y PDF"
git push origin main
```

### 7\. Documentación

Se creó este `README.md` y se verificó el historial con `git log --oneline`.

## Registro de cambios (commits)

|Orden|Mensaje de commit|Archivos|
|-|-|-|
|1|Agrega README.md inicial con descripción de la actividad|README.md|
|2|Agrega capítulo 1 (Inicio) del tutorial de Git en Word y PDF|docs/01-\*|
|3|Agrega capítulo 2 (Fundamentos de Git) en Word y PDF|docs/02-\*|
|4|Agrega capítulo 3 (Ramificaciones en Git) en Word y PDF|docs/03-\*|
|5|Agrega capítulo 4 (Git en el Servidor) en Word y PDF|docs/04-\*|
|6|Agrega capítulo 5 (Git en entornos distribuidos) en Word y PDF|docs/05-\*|
|7|Agrega capítulo 6 (GitHub) en Word y PDF|docs/06-\*|
|8|Agrega capítulo 7 (Herramientas de Git) en Word y PDF|docs/07-\*|
|9|Agrega capítulo 8 (Personalización de Git) en Word y PDF|docs/08-\*|
|10|Agrega capítulo 9 (Git y Otros Sistemas) en Word y PDF|docs/09-\*|
|11|Agrega capítulo 10 (Entresijos internos de Git) en Word y PDF|docs/10-\*|
|12|Actualiza README.md con el registro de commits y comandos usados|README.md|

(El historial real se puede consultar con `git log --oneline` o en la pestaña **Commits** de GitHub.)

## Comandos de Git utilizados

|Comando|Para qué se usó|
|-|-|
|`git config`|Configurar nombre, correo y rama por defecto|
|`git clone`|Clonar el repositorio remoto|
|`git status`|Ver el estado de los archivos|
|`git add`|Preparar archivos para el commit|
|`git commit -m`|Confirmar cambios con mensaje descriptivo|
|`git push`|Enviar los commits a GitHub|
|`git log --oneline`|Revisar el historial|
|`git diff`|Revisar cambios antes de confirmar|

## Convención de mensajes de commit

* Verbo en presente (*Agrega, Actualiza, Corrige*).
* Qué se hizo y sobre qué archivo o capítulo, en una sola línea corta.
* Un commit por cada cambio lógico (un capítulo = un commit).

## Entregables relacionados

* Informe de proceso (PDF) con pantallazos, dificultades, soluciones y conclusión.
* Enlace del repositorio: https://github.com/requiempax/Practica-ciencia-datos-practica-2

## Referencias

* Chacon, S., \& Straub, B. (2014). *Pro Git* (2nd ed.). Apress. https://git-scm.com/book/es/v2
* Hutch Data Science. (n.d.). *Using GitHub in a workflow*.
* GitHub, Inc. (2019). *GitHub Guides: Learn Git and GitHub*.


\## Verificación final

Historial comprobado con `git log --oneline` el 14/10/2026: 10 capítulos subidos en commits separados, uno por capítulo, más el commit del README.

