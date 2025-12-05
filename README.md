Ex01 Django ORM Web Application
Date: 05/12/2025
Ref no: 25014734

## AIM
To develop a Django Application to store and retrieve data from a E-Commerce Website Database for Amazon or Flipkart using Object Relational Mapping(ORM).

DESIGN STEPS

STEP 1:
Clone the problem from GitHub

 STEP 2:
Create a new app in Django project

 STEP 3:
Enter the code for admin.py and models.py

STEP 4:
Detect changes and create migration files that describe how to modify the database schema

STEP 5:
Execute the migration files and update the database schema to match your Django models

 STEP 6:
Create a superuser with full access rights to all models and data through the admin interface.

 STEP 7:
Apply the migration files of the created app to the database

 STEP 8:
Execute Django admin using localhost and create details for 10 entries

 PROGRAM
admin.py
python
from django.contrib import admin
from .models import Product, ProductAdmin

admin.site.register(Product, ProductAdmin)

 models.py
python
from django.db import models
from django.contrib import admin

class Product(models.Model):
    product_id = models.CharField(max_length=20, primary_key=True)
    name = models.CharField(max_length=100)
    category = models.CharField(max_length=50)
    price = models.DecimalField(max_digits=10, decimal_places=2)
    rating = models.FloatField()
seller = models.CharField(max_length=100)
    stock = models.IntegerField()
    offer = models.CharField(max_length=50, blank=True)
    delivery_date = models.DateField()

class ProductAdmin(admin.ModelAdmin):
    list_display = (
        'product_id',
        'name',
        'category',
        'price',
        'rating',
        'seller',
        'stock',
        'offer',
        'delivery_date',
    )


 OUTPUT
<img width="1918" height="974" alt="Screenshot 2025-12-03 170334" src="https://github.com/user-attachments/assets/ed3ba562-adfc-4e79-b6a9-76a03007e550" />

RESULT
Thus the program for creating E-commerce website database using ORM hass been executed successfully
