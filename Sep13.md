## Started with breakout rooms
How is views different with drf?
    -class based
What is a serializer?
    -translates into something the FE can understand, JSON, etc.
What is an endpoint?
    -allows FE software to communicate with server, like templates but API's don't have templates

## Amy's Habit Tracker example
_Get used to Insomnia, check out Postman as well_
__Insomnia__
works as a client, when setting up as a GET request, it will show you want the User/Client will see

Can look at source code, raw data

_if you get HTML then your endpoint is sending HTML so that could be wrong_

__REST_FRAMEWORK in settings__
holds a list with a key DEFAULT_PERMISSION_CLASSES and a str value of rest_framework.permissions.DjangoModelPermissionsOrAnonReadOnly

__Django allows for multiple apps in the same project__
created a new app called 'api'

don't need to make new models if its a second app, can just use the models from the first app

created a urls.py in the app for the api urls

added a url pattern, can create the views later, or vice versa, after the url pattern is made, you can test it on insomnia



