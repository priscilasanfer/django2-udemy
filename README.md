
### Iniciar o projeto
> pip install django whitenoise gunicorn django-bootstrap4 PyMySQL django-stdimage


Whitenoise: Após publicar o app é possível apresentar os arquivos estáticos  
Gunicorn: rodar o servidor HTTP   
django-bootstrap4: forma facilitada para usar o bootstrap ja integrado com o django   
PyMySQL: driver de conexão com o Python e o MySql  
Django-stdimage: aplicacao que facilita a trabalhar com imagens   


### Criar o arquivo de requirements: 
> pip freeze > requirements.txt

### Criar projeto
> django-admin startproject django2 .

### Criar aplicação
> django-admin startapp core 

### MySql Docker
> docker run -it --name mysql -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 -d mysql

### Rodar a aplicação
> python manage.py runserver

### Criar migration
> python manage.py migrate 
> docker-compose exec web python manage.py migrate 

### Criar super usuario
> python manage.py createsuperuser
> docker-compose exec web python manage.py createsuperuser

### Fazer a migracao
> python manage.py makemigrations
> docker-compose exec web python manage.py makemigrations 


### Preparando o projeto para o deploy no heroku
> heroku login
> arquivo runtime.txt 
> arquivo Procfile

### Criando aplicação no Heroku
> heroku create django2-prisanfer --buildpack heroku/python

### Deploy no Heroku
> git push heroku main

### Realizar migrate
> heroku run python manage.py migrate

### Criar superuser no heroku
> heroku run python manage.py createsuperuser

### Verificar se nao falta nada a ser instalado 
> pip install -r requirements.txt   

### Zerar banco de dados no heroku
> heroku ps:reset DATABASE_URL
