## heroku_django ##

    1. Instale o Heroku Toolbelt:

        wget -qO- https://toolbelt.heroku.com/install.sh | sh

    2. Faça o login:

        $ heroku login
            Enter your Heroku credentials.
            Email: gladson@immensa.com.br
            Password (typing will be hidden): 123456789
            Found existing public key: /home/casa/.ssh/id_rsa.pub
            Uploading SSH public key /home/casa/.ssh/id_rsa.pub... done
            Authentication successful.

    3. faça o virtualenv:

        $ virtualenv --no-site-packages env
            New python executable in env/bin/python
            Installing setuptools............done.
            Installing pip...............done.

    4. Ative o virtualenv:

        $ source env/bin/activate

    5. Instale os pacotes no virtualenv:

        $ pip install -r requirements.txt

    Obs.: Caso de problema na instalação:
    $ sudo apt-get install libpq-dev python-dev

    6. Teste se tudo, Ok?

        $ ./manage.py runserver localhost:8000

    7. Crie uma app no Heroku:

        $ heroku create sua-app-django

    8. Envie a sua app:

        $ git push heroku master

    9. Sincronizar banco de dados:

        $ heroku run python manage.py syncdb

        $ heroku run python manage.py collectstatic
