# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

### STEP 1:
   Clone the repository from github

### STEP 2:
   Create an admin page for Django.

### STEP 3:
   create an app and edit settings.py

### STEP 4:
   Makemigration and migrate the changes.

### STEP 5:
   Create admin user and write python code for admin and models

### STEP 6:
   Make all the migration to my app

### STEP 7:
   Create a students database with 10 fields using runservercommand
admin.py


## PROGRAM

```py
from django.db import models
from django.contrib import admin

# Create your models here.
class Student(models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text='Employee ID')
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    contact=models.IntegerField()

class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','contact')    
```
```py
from django.contrib import admin
from .models import Student,StudentAdmin

admin.site.register(Student,StudentAdmin)
```    

## OUTPUT



![Student list](https://github.com/22009058/django-orm-app/assets/121917232/7c0a6199-9d62-4a23-be3b-ab0692e80db3)

## RESULT
The program for creating a studentdatabase using ORM is executed successfully.
