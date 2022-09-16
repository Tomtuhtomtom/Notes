# Things to keep in mind

1. Django doesn't work in steps
2. Treat it like an escape room
3. Be bold enough to try stuff, don't worry about breaking things

## Postgresql database setup

For settings.py, if not using .env, you can write it out like so:

DATABASES = {
    "default": {
        "ENGINE": 'django.db.backends.postgresql',
        "NAME": 'example',
        "USER": 'example',
        "HOST": 'localhost',
        "PORT": '5432',
    }
}

Same info in .env, just different syntax

_quick tip: press the period button on github and it will bring up a virtual VSC to look at the code_

__Download Postico__

## Django refresher

Start with models, good to draw them out.  Using the Django music example, we have User, Artist, Album and Genre

In the class CustomUser, the argument in the () is what it inhereits from, so CustomUser(AbstractUser) is inhereiting from AbstractUser and CustomUser is able to use that data

__Take advantage of Excalidraw__

When building models, it doesn't have to relate to the real world, it needs to work for your app.  For example, when two artist colabralate on an album, one way to do it is to create a third artist which includes both artists.  

ForeignKey (FK) is one to many so in the Album model, artist is a field with a FK since one artist can have many albums

ManyToMany (M2M) for example in the Album model, genre is a field with a M2M since many albums can have many genres

_random side question: What is a slug?_
_a slug is a short label, generally used in URLs_
_*refer to docs.djangoproject.com for all the different field types_

## View functions

request is a django object so we use request in the () of the function because that is the object uses when viewing a url, example:
_def home(request):_

Other parts of the function we need to know,
def home(request):
    if request.user.is_authenticated:
        return redirect('list_albums')
    return render(request, 'music/home.html')

so the if statement checks if user is logged in and if so, redirects to the url path named list_albums and if not logged in, renders the music/home.html page

_tip: you can give imports names for example:_
_from music import views as music_views_
_* this is nice if you have multiple apps in the same project_

## Review function below

@login_required
def list_albums(request):
    sort_by = request.GET.get("sort") or "title"
    albums = Album.object.annotate(
        favorited=Exists(
            CustomUser.objects.filter(
                favorite_albums=OuterRef("pk"), pk=request.user.pk
            )
        )
    ).order_by(sort_by)

## python shell

In terminal, use python manage.py shell or if you've installed django-extensions you can use python manage.py shell_plus and it will load all your imports automatically

__queries__
Examples:
Album.objects.all()    .filter()    .count() 
_Modelname.objects.queryfunction()_
go to django-queries.md on class website for more
__new entries__
new_artist = Artist(name="The Beatles")
_variable = Model(field="")_
until you save it, it will not have a pk and won't be in your database
new_artist.save()


## Planning models

answer the question, what does this app do?  What will the user tell the app what they want from the app?

For Habit Tracker
I want to read 40 pages a day
Break down the nouns, I(User), to read(Habit), 40 pages(Goal)

