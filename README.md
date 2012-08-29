heroku_django
=============

I. Instale o Heroku Toolbelt:

wget -qO- https://toolbelt.heroku.com/install.sh | sh

II. Faça o login:

$ heroku login
Enter your Heroku credentials.
Email: gladson@agronomo.eng.br
Password (typing will be hidden): 123456789
Found existing public key: /home/casa/.ssh/id_rsa.pub
Uploading SSH public key /home/casa/.ssh/id_rsa.pub... done
Authentication successful.

III. faça o virtualenv:

$ virtualenv --no-site-packages env
New python executable in env/bin/python
Installing setuptools............done.
Installing pip...............done.

IV. Ative o virtualenv:

$ source env/bin/activate

V. Instale os pacotes no virtualenv:

$ pip install -r requirements.txt

Obs.: Caso de problema na instalação:
$ sudo apt-get install libpq-dev python-dev

VI. Teste se tudo, Ok?

$ ./manage.py runserver localhost:8000

VII. Crie uma app no Heroku:

$ heroku create sua-app-django

VIII. Envie a sua app:

$ git push heroku master

IX. Sincronizar banco de dados:

$ heroku run python manage.py syncdb

$ heroku run python manage.py collectstatic