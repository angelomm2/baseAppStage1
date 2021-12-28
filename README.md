# baseAppStage1
Base app - backend

# version python
3.8.10

# version django
4.0

# requirements 
djangorestframework,
psycopg2 python module requiered for postgreSql

# validate django version
python3 -c "import django; print(django.get_version())"

# timezone config(settings.py) 
USE_TZ = False  # change if needed
TIME_ZONE = 'UTC'

# code language(settings.py)
LANGUAGE_CODE = 'en-us'  # change if needed

# set config for password validation(settings.py)
AUTH_PASSWORD_VALIDATORS = [  # set as preferred
    {
        'NAME': 'django.contrib.auth.password_validation.UserAttributeSimilarityValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.MinimumLengthValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.CommonPasswordValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.NumericPasswordValidator',
    },
]


# set DDBB config(settings.py)
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'OPTIONS': {
            'service': 'my_service',  # change it
            'passfile': '.my_pgpass',  # change it
        },
    }
}

# views.py
handler controller for classes, example: authentication class
