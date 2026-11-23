Aquí tienes una propuesta completa y lista para copiar y pegar en tu archivo `README.md`. Está redactada en formato Markdown para que se vea bien estructurada en GitHub.

# Aprendiendo Git y GitHub

Este repositorio documenta mis primeros pasos utilizando **Git** para el control de versiones y **GitHub** para alojar el código en la nube, realizando todo el flujo de trabajo directamente desde la terminal.

## Estructura del proyecto

El entorno de trabajo local se encuentra en la carpeta `githubentorno` y contiene los siguientes archivos:

```text
githubentorno/
├── prueba.txt
└── README.md
```

---

## Proceso y comandos utilizados

A continuación se detallan los comandos ejecutados paso a paso desde la inicialización del repositorio hasta la subida del primer _commit_ a GitHub:

### 1. Preparar el entorno local

Accedemos a la carpeta del proyecto e inicializamos un nuevo repositorio de Git.

```bash
cd githubentorno
git init

```

### 2. Cambiar el nombre de la rama principal (Opcional / Recomendado)

Nos aseguramos de que la rama principal se llame `main` para coincidir con el estándar actual de GitHub.

```bash
git branch -M main

```

### 3. Preparar y confirmar los archivos (Primer Commit)

Añadimos el archivo de prueba al área de preparación (_staging area_) y guardamos los cambios en el historial local con un mensaje descriptivo.

```bash
git add prueba.txt
git commit -m "Primer commit: añadir prueba.txt"

```

### 4. Crear el repositorio en GitHub desde la terminal y subir los cambios

Utilizando la herramienta oficial **GitHub CLI (`gh`)**, creamos el repositorio remoto directamente desde la consola, lo vinculamos con nuestra carpeta local y subimos el código (`--push`):

```bash
gh repo create githubentorno --public --source=. --remote=origin --push

```

_(Nota: Si se creó como privado, se utilizó `--private` en lugar de `--public`)._

---

## Comandos útiles de verificación

Durante el proceso, estos comandos sirven para comprobar que todo está en orden:

- `git status`: Muestra el estado de los archivos (si están sin seguimiento, preparados o confirmados).
- `git log --oneline`: Muestra el historial resumido de los _commits_ realizados.
- `git remote -v`: Verifica que la carpeta local esté conectada correctamente con la URL de GitHub.
