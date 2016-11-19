# laravel-django-cheatsheet
A translation reference for Laravel and Django

|   	|   Laravel 5.x	|   Django 1.9.x	|   Django Docs	|   	|
|---	|---	|---	|---	|---	|
|   **URLS**	|   	|   	|   	|
|   	|   	|   	|   	|
|   Concept	|   All routes contained in `routes.php` <br>[[Docs](https://laravel.com/docs/5.3/routing#basic-routing)]	|   The convention is to create a URLconf	and import the views at `urls.py`|   [Urlconf](https://docs.djangoproject.com/en/1.10/topics/http/urls/#id4)	|
|   Named Routes	|   `Route::get('user/profile', 'UserController@showProfile')->name('profile');`	|   `urlpatterns = [` <br>&nbsp;&nbsp;&nbsp;&nbsp;`url(r'^articles/2003/$', views.special_case_2003)`<br>`]`	|   [Named Groups](https://docs.djangoproject.com/en/1.10/topics/http/urls/#named-groups)	|
|   	|   	|   	|   	|
|  **Working with Models**	|   	|   	|   	|
|       |   	|   	|   	|
| Create |   ````Post::create($object);````	|   ````Post.objects.create(user=user, title=“Some title”)````	|   	|
|  Get a collection of objects 	|   ````Post::where(id,5)->get();````	|   ````Post.objects.filter(id=4)```` OR ````obj = get_object_or_404(Comment, id)````	|   	|
|   Get the first object	|   ````Post::first();````	|   ````Post.objects.first()````	|   	|
|   	|   Concept: Polymorphic one to many relation [[Docs](https://laravel.com/docs/5.3/eloquent-relationships#polymorphic-relations)]	|   Concept: Generic Foreign Keys	|   [Generic Relations](https://docs.djangoproject.com/en/1.10/ref/contrib/contenttypes/#generic-relations)	| 
|       |   	|   	|   	|
|  **Auth** 	|   	|   	|   	|
|       |   	|   	|   	|
|       |   ````$user = Auth::user();````	|   ````{{request.user}}````	|   [User Objects](https://docs.djangoproject.com/en/dev/topics/auth/default/#user-objects)	|
|   	|   ````return redirect()->intended('dashboard’);````	|   ```` next = request.GET.get('next') ````<br> ````if next:````<br>&nbsp;&nbsp;&nbsp;&nbsp;````return````<br>````redirect(next)````	|   	|
|   **Pagination**    |   	|   	|   	|
|       |   	|   	|   [DRF Docs](http://www.django-rest-framework.org/api-guide/pagination/)	|

|   	|   	|   	|   	|