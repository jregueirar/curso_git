# curso_git

### Deploy entorno de desarrollo

- Ejecutar el siguiente script o comandos desde una terminal linux

```
#!/bin/bash

APP_DIR=~/curso_git
VENVS_DIR=~/venvs

cd $APP_DIR
git clone https://github.com/jregueirar/curso_git.git $APP_DIR

cd $VENVS_DIR
virtualenv-3.5 curso_git
source $VENVS_DIR/curso_git/bin/activate

cd $APP_DIR
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver 0.0.0.0:8000

```

- Abrir un navegador en la dirección http://127.0.0.1:8000

- Django administration:
  - Crear superusuario: python manage.py createsuperuser
  - http://127.0.0.1:8000/admin

### Requisitos Tarea

- Crear repositorio en github.
- Web de una compañia
  - Tres páginas, una que sea la página del equipo (quienes somos)
  - Sistema de Login
  - Formulario de contacto
  - Que haga uso de CSS
  - Que se vea que hacemos commits, merges,..
    - Al menos 2 versiones (TAGs) - nomenclatura vX.x
    - Al menos 2 ramas
