# Django errors


### Table of Contents
* [Import Error](#import-error)
* [Name Error](#name-error)
* [Attribute Error](#attribute-error) 

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


<br>
---
<center>[Home](README.md) | [Top](#django-errors)</center>
