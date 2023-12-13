La tarea fue realizada con replit.com y la base de datos está alojada en vercel.com.
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'login_app',
        'USER': 'default',
        'PASSWORD': 'JBzrA1SN6pbj',
        'HOST': 'ep-super-art-48444499.us-east-1.postgres.vercel-storage.com',
        'PORT': '5432',
        'OPTIONS': {
            'sslmode': 'require',
        },
    }
}

Se puede cambiar a modo local reemplazando en settings.py por:
DATABASES = { 'default': { 'ENGINE': "django.db.backends.postgresql", 'NAME': 'nombre', 'USER': 'user', 'PASSWORD': 'password', 'HOST': 'localhost', 'PORT': '5432', } }

Posteriormente hay que volver a inicializar la base de datos:
$ cd loginTask
$ createdb login_task
$ python manage.py migrate
