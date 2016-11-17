# laravel-django-cheatsheet
A translation reference for Laravel and Django

|   	|   Laravel 5.x	|   Django 1.9.x	|   Django Docs	|   	|
|---	|---	|---	|---	|---	|
|   	|   	|   	|   	|   	|
|  **Working with Models**	|   ````Post::create($object);````	|   ````Post.objects.create(user=user, title=“Some title”)````	|   	|   	|
|  Get a collection of objects 	|   ````Post::where(id,5)->get();````	|   ````Post.objects.filter(id=4)```` OR ````obj = get_object_or_404(Comment, id)````	|   	|   	|
|   Get the first object	|   ````Post::first();````	|   ````Post.objects.first()````	|   	|   	|
|   	|   Concept: Polymorphic one to many relation [Docs]	|   Concept: Generic Foreign Keys	|   [Generic Relations](https://docs.djangoproject.com/en/1.10/ref/contrib/contenttypes/#generic-relations)	|   	|

|   	|   	|   	|   	|   	|