Iniciar o projeto Django

```
pythonn -m venv venv
. venv/Scripts/activate
pip install Django
django-admin startproject project .
python manage.py startapp contact
```

configurar o git

```
git config --global user.name 'Seu nome'
git config --global user.email 'Seu email'
git config --global user.defaultBranch main
git init
git add .
git commit -m 'Mensangem'
git remote add origin URL_DO_GIT

```

Migrando a base  de dados do Django - Migrations
Base de dados do app


```
python manage.py makemigrations
python manage.py migrate
```

```

Criando e modificando a senha de um super usuário Django

```

```
python manage.py createsuperuser
python manage.py changepassword USERNAME
```