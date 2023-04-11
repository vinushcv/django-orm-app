# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![orm er ](https://user-images.githubusercontent.com/113975318/231061388-aa68e1b2-5be8-4629-8449-85ff4926df71.png)



## DESIGN STEPS

### STEP 1:
Clone the git repository from github

### STEP 2:
Create an admin interface for Django

### STEP 3:
Create an app and edit the settings.py

### STEP 4:
Makemigrations and migrate the changes 

### STEP 5:
Create admin user and write python code for admin and models

### STEP 6:
Make all the migrations to 'myapp'

### STEP 7:
Create an employee table to fit 5 fields using runserver command


## PROGRAM
```python
admin.py:
from django.contrib import admin
from .models import Student,StudentAdmin,Employee,EmployeeAdmin
admin.site.register(Student,StudentAdmin)
admin.site.register(Employee,EmployeeAdmin)

models.py:
from django.db import models
from django.contrib import admin



class Student (models.Model):
    referencenumber=models.CharField(max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email')

class Employee (models.Model):
    emp_id=models.CharField(primary_key=True,max_length=4,help_text='Employee ID')
    ename=models.CharField(max_length=50)
    post=models.CharField(max_length=20)
    salary=models.IntegerField()


class EmployeeAdmin(admin.ModelAdmin):
    list_display=('emp_id','ename','post','salary')
```


## OUTPUT
![orm out](https://user-images.githubusercontent.com/113975318/231060267-6cd13d8b-1e5c-4eb0-944a-12d18e96171d.png)




## RESULT
The program for creating an employee database using ORM is executed successfully
