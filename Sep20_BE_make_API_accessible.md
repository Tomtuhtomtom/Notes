## We need to make the API accessible exclusively to the FE
CORS is built in (Cross Origin Resource Sharing)
We need to use a library django-cors-headers 3.13.0
pip install django-cors-headers (use pipenv)

add corsheaders to installed_apps

add corsheaders.middleware.CorsMiddleware to the MIDDLEWARE above django.middleware.common.CommonMiddleware

add CORS_ALLOWED_ORIGINS = [] or
Recommended for this project:
add CORS_ALLOW_ALL_ORIGINS = True
