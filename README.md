<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

# Nest-MicroServices - Launcher

Repositorio para el Launcher de la aplicación Products realizada en [Nest](https://github.com/nestjs/nest). 
Basado en el curso de "NestJs + Microservicios: Aplicaciones escalables y modulares" de [DevTalles](https://cursos.devtalles.com/) en Udemy.

## Pasos para el desarrollo

1. Clonar el repositorio

2. Crear un archivo ```.env``` basado en ```.env.template```.

3. Reconstruir los sub-módulos

```bash
$ git submodule update --init --recursive
```

4. Crear los contenedores Docker

```bash
$ docker compose up --build
```

## Aspectos estudiados

En este repositorio se trabajan los siguientes aspectos de Nest con microservicios:
- Levantar todos los microservicios con un único comando
- Expandir el custom exception filter
- Crear un repositorio con submódulos

## Pasos para crear los Git Submodules

1. Crear un nuevo repositorio en GitHub

2. Clonar el repositorio en la máquina local

3. Añadir el submodule, donde `repository_url` es la url del repositorio y `directory_name` es el nombre de la carpeta donde se guarda el sub-módulo (no debe de existir en el proyecto)

```bash
$ git submodule add <repository_url> <directory_name>
```

4. Añadir los cambios al repositorio (git add, git commit, git push)
Ej:
``` bash
$ git add .
$ git commit -m "Add submodule"
$ git push
```

5. Inicializar y actualizar Sub-módulos, cuando alguien clona el repositorio por primera vez, debe de ejecutar el siguiente comando para inicializar y actualizar los sub-módulos

```bash
$ git submodule update --init --recursive
```

6. Para actualizar las referencias de los sub-módulos

```bash
$ git submodule update --remote
```

### Importante
Si se trabaja en el repositorio que tiene los sub-módulos, **primero actualizar y hacer push** en el sub-módulo y **después** en el repositorio principal. 

Si se hace al revés, se perderán las referencias de los sub-módulos en el repositorio principal y habrá que resolver conflictos.

