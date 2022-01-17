
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



### Deploy heroku
> heroku login
> arquivo runtime.txt 
> arquivo Procfile
> 
