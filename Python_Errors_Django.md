# Django errors


### Table of Contents
* [Import Error](#import-error)
* [Name Error](#name-error)
* [Attribute Error](#attribute-error) 
* [TemplateDoesNotExist Error](#templatedoesnotexist-error)
* [Forbidden 403](#forbidden-403)
* [DoesNotExist Error](#doesnotexist-error)


-----------------------

## Import Error

```bash
ImportError: No module named apps
```

* You are missing your __init__.py (dunder init) file inside your apps folder. Use `touch` in the terminal to create it.

```bash
touch apps/__init__.py
```
-----------------------

```bash
ImportError: No module named urls
```
* You either misspelled your file/location or did not create it.

-----------------------

```bash
ImportError: No module named APPdjango.contrib
```
* You are missing a comma in `INSTALLED_APPS` in your settings.py file.

-----------------------

## Name Error

```bash
NameError: name 'include' is not defined
```
* You are missing your import for include. This is in your PROJECT/urls.py file.

```python
from django.conf.urls import url, include
```
-----------------------


```bash
NameError: name 'views' is not defined
```
* You forgot to import your views.py file in your urls.py.

```python
from . import views
```
-----------------------

## Attribute Error

```bash
AttributeError: 'module' object has no attribute 'index'
```
* You forgot to create your index method or misspelled it in your views.py file.
```python
def index(request):
  pass
```
-----------------------

## TemplateDoesNotExist Error

```
TemplateDoesNotExist at /
```

* You could have a problem with your templates directory. The correct format is `apps/APPNAME/templates/APPNAME/index.html`.

```bash
mkdir apps/APPNAME/templates
mkdir apps/APPNAME/templates/APPNAME
touch apps/APPNAME/templates/APPNAME/index.html
```

* You could have forgotten to add your app to the `INSTALLED_APPS` in settings.py.

```python
INSTALLED_APPS = [
    'apps.APPNAME',
    'django.contrib.admin',
]
```
-----------------------
<br>
## Forbidden 403

```
Forbidden (403)
CSRF verification failed. Request aborted.
```
* You CSRF token is missing or incorrect.
```html
<form action="/logout" method="post">
  {% csrf_token %}
  <input type="submit" value="Log out">
</form>
```
-----------------------

## DoesNotExist Error

```
DoesNotExist at /
User matching query does not exist.
```
* You are probably missing a try/except for a `User.objects.get(id=id)`. Use `User.objects.filter(id=id)` instead and access the first element with [0].



---
[Home](README.md) | [Top](#django-errors)
