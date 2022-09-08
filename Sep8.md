## Started off with review of where everyone is at
_*tip for debugging, read the bottom line, then go up lines until you hit a file you've changed_

Don't worry about CRUD(look this up later), don't worry about edit and delete until you have some working features, get the user to add habits and add records first

Use the trifecta, views, urls, templates and do ONE at a time, don't copy and paste 4 things at once and change the nouns-bigger chance of creating bugs

__Priority for today__
create habits and list habits

_suggestion_
list of records can be in the habit detail as a history and can become a chart

_*Remember the pet collar example for foreignkeys, the pets where a tag with the same phone number for the owner_

## Recipe Book Example
added a logging block of code for SQL in the settings.py, need to learn more about that

__For URL with date in it__
you can bring in year=, month=, day= in your views
and bring <int:year> etc. in your urlpattern

in the views function:
if year is None:
    date_for_plan = datetime.date.today()
else:
    date_for_plan = datetime.date(year, month, day)
next_day = date_for_plan + datetime.timedelta(days=1)
prev_day = date_for_plan + datetime.timedelta(days=-1)

_there is another line here for get_or_create()

in models.py:
constraints = [
    UniqueConstraint(fields=['user', 'date'], name='unique_user_date')
]

__Go to docs.djangoproject.com/en/4.0/ref/models/options/#constraints for more info__


