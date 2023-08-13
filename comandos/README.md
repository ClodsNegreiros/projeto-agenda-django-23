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

```
Trabalhando com o model do Django

# importe o módulo
from contact.models import Contact
# Cria um contato  (Lazy)

# Retorna o contato
contact = Contact(**fields)

contact.save()
# Cria um contato (Não Lazy)

# Retorna o contato
contact = Contact.objects.create(**fields)

# Seleciona um contato com id 10
# Retorna o contato
contact = Contact.objects.get(pk=10)

# Edita um contato
# Retorna o contato
contact.field_name1 = 'Novo valor 1'
contact.field_name2 = 'Novo valor 2'
contact.save()

# Apaga  um  contato
# Depende da base de dados,  geralmente retorna o número
#    de valores manipulados na base de dados
contact.delete()

# Seleciona todos contatos ordenados por id DESC
# Retorna QuerySet[]
contacts = Contact.objects.all().order_by('-id')

# Seleciona contatos usando    filtros
# Retorna QuerySet[]
contacts = Contact.object.filter(**filters).order_by('-id')
```