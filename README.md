# 🚀 Django Framework Step-by-Step Learning Guide

> Complete Beginner to Advanced Django Roadmap  
> Everything is organized in table format inside a single Markdown file.

---

# 📚 Table of Contents

| Step | Topic |
|---|---|
| 1 | Introduction to Django |
| 2 | Install Python & Django |
| 3 | Create First Django Project |
| 4 | Understanding Django Project Structure |
| 5 | Create Django App |
| 6 | Django URLs |
| 7 | Django Views |
| 8 | Django Templates |
| 9 | Static Files |
| 10 | Models & Database |
| 11 | Django Admin Panel |
| 12 | Django ORM |
| 13 | Forms |
| 14 | User Authentication |
| 15 | CRUD Application |
| 16 | Class Based Views |
| 17 | Django REST Framework |
| 18 | Authentication APIs |
| 19 | File Uploads |
| 20 | Deployment |

---

# 1️⃣ Introduction to Django

| Topic | Details |
|---|---|
| What is Django? | Django is a high-level Python web framework used to build secure and scalable web applications quickly. |
| Language Used | Python |
| Architecture | MVT (Model View Template) |
| Main Features | ORM, Admin Panel, Authentication, Security, Scalability |
| Best For | Web apps, APIs, Dashboards, Enterprise systems |

---

# 2️⃣ Install Python & Django

| Step | Command |
|---|---|
| Install Python | `brew install python` |
| Check Python | `python3 --version` |
| Create venv | `python3 -m venv venv` |
| Activate venv | `source venv/bin/activate` |
| Install Django | `pip install django` |
| Verify Django | `django-admin --version` |

---

# 3️⃣ Create First Django Project

| Command | Description |
|---|---|
| `django-admin startproject myproject` | Create project |
| `cd myproject` | Enter project folder |
| `python manage.py runserver` | Start server |

---

# 4️⃣ Understanding Django Project Structure

| File/Folder | Purpose |
|---|---|
| `manage.py` | Django command utility |
| `settings.py` | Project settings |
| `urls.py` | URL routing |
| `wsgi.py` | Production configuration |
| `asgi.py` | Async configuration |

---

# 5️⃣ Create Django App

| Command | Purpose |
|---|---|
| `python manage.py startapp myapp` | Create app |

## Add App in settings.py

```python
INSTALLED_APPS = [
    'myapp',
]
```

---

# 6️⃣ Django URLs

```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.home),
]
```

---

# 7️⃣ Django Views

```python
from django.http import HttpResponse

def home(request):
    return HttpResponse("Hello Django")
```

---

# 8️⃣ Django Templates

| Folder | Purpose |
|---|---|
| `templates/` | Store HTML files |

```python
from django.shortcuts import render

def home(request):
    return render(request, 'home.html')
```

```html
<h1>Welcome to Django</h1>
```

---

# 9️⃣ Static Files

| Type | Examples |
|---|---|
| CSS | Styling |
| JS | JavaScript |
| Images | Logos |

```python
STATIC_URL = 'static/'
```

---

# 🔟 Models & Database

```python
from django.db import models

class Post(models.Model):
    title = models.CharField(max_length=100)
    content = models.TextField()
```

| Command | Purpose |
|---|---|
| `python manage.py makemigrations` | Create migration |
| `python manage.py migrate` | Apply migration |

---

# 1️⃣1️⃣ Django Admin Panel

| Command | Purpose |
|---|---|
| `python manage.py createsuperuser` | Create admin |

```python
from django.contrib import admin
from .models import Post

admin.site.register(Post)
```

---

# 1️⃣2️⃣ Django ORM

| Query | Purpose |
|---|---|
| `Post.objects.all()` | Get all records |
| `Post.objects.get(id=1)` | Get one record |
| `Post.objects.filter(title='Test')` | Filter records |
| `post.save()` | Save object |
| `post.delete()` | Delete object |

---

# 1️⃣3️⃣ Django Forms

```python
from django import forms

class ContactForm(forms.Form):
    name = forms.CharField(max_length=100)
```

---

# 1️⃣4️⃣ User Authentication

| Feature | Supported |
|---|---|
| Login | ✅ |
| Logout | ✅ |
| Registration | ✅ |
| Password Hashing | ✅ |

---

# 1️⃣5️⃣ CRUD Application

| Operation | Meaning |
|---|---|
| Create | Add data |
| Read | Display data |
| Update | Edit data |
| Delete | Remove data |

---

# 1️⃣6️⃣ Class Based Views

| View | Purpose |
|---|---|
| `ListView` | Show list |
| `DetailView` | Show details |
| `CreateView` | Create object |
| `UpdateView` | Update object |
| `DeleteView` | Delete object |

---

# 1️⃣7️⃣ Django REST Framework

| Command | Purpose |
|---|---|
| `pip install djangorestframework` | Install DRF |

```python
INSTALLED_APPS = [
    'rest_framework',
]
```

---

# 1️⃣8️⃣ Authentication APIs

| API Type | Usage |
|---|---|
| JWT Authentication | Modern APIs |
| Token Authentication | Mobile Apps |
| Session Authentication | Web Apps |

---

# 1️⃣9️⃣ File Uploads

```python
MEDIA_URL = '/media/'
MEDIA_ROOT = BASE_DIR / 'media'
```

---

# 2️⃣0️⃣ Deployment

| Platform | Difficulty |
|---|---|
| Render | Easy |
| Railway | Easy |
| AWS | Medium |
| Docker | Medium |

---

# ⚡ Important Django Commands Cheat Sheet

| Command | Purpose |
|---|---|
| `python manage.py runserver` | Start server |
| `python manage.py migrate` | Apply migrations |
| `python manage.py makemigrations` | Create migrations |
| `python manage.py createsuperuser` | Create admin |
| `python manage.py shell` | Open shell |
| `python manage.py collectstatic` | Collect static files |
| `python manage.py startapp appname` | Create app |
| `django-admin startproject projectname` | Create project |

---

# 🎯 Final Goal

| Goal |
|---|
| Build Full Stack Django Applications |
| Build REST APIs |
| Deploy Production Applications |
| Become Django Backend Developer |

---

# 🏁 End of Guide