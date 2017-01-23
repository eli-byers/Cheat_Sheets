# Django errors


### Table of Contents
* [Import Error](#import-error)
* [Name Error](#name-error)
* [Attribute Error](#attribute-error) 
* [TemplateDoesNotExist Error](#TemplateDoesNotExist-error) 

-----------------------
<br>
## Import Error

```bash
ImportError: No module named apps
```

* You are missing your __init__.py (dunder init) file inside your apps folder. Use `touch` in the terminal to create it.

```bash
touch apps/__init__.py
```
-----------------------
<br>
```bash
ImportError: No module named urls
```
* You either misspelled your file/location or did not create it.

-----------------------
<br>
```bash
ImportError: No module named APPdjango.contrib
```
* You are missing a comma in `INSTALLED_APPS` in your settings.py file.

-----------------------
<br>
## Name Error

```bash
NameError: name 'include' is not defined
```
* You are missing your import for include. This is in your PROJECT/urls.py file.

```python
from django.conf.urls import url, include
```
-----------------------
<br>

```bash
NameError: name 'views' is not defined
```
* You forgot to import your views.py file in your urls.py.

```python
from . import views
```
-----------------------
<br>
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
<br>
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

<br>
---
<center>[Home](README.md) | [Top](#django-errors)</center>
