## Started off in breakout Rooms
Discussed light bulb moments and rabbit holes that we ran into

## Worked in python shell
was able to show how we can import our models and run queries to check if we collected the right data

_*tip: .filter() brings back a queryset whereas .get() brings back the object_
So, .filter() shows QuerySet [<key: value>]
.get() shoes <key: value>

## get_or_create
Amy put a breakpoint() in a function and in the terminal can run the command locals() to see what is available within that function

dir(request) shows all the things that you can access with request, not just request.user

_*side note, in Amy's recipe example, request.user.meal_plans, meal_plans is the related name in the model*_

