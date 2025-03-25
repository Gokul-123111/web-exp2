# Ex02 Django ORM Web Application
# Date:25\03\2025
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
admin.py
```
from django.contrib import admin
from .models import Loan,LoanAdmin

admin.site.register(Loan,LoanAdmin)
```
models.py
```
from django.db import models
from django.contrib import admin

class Loan(models.Model):
    loan_id = models.AutoField(primary_key=True)
    customer_name = models.CharField(max_length=100)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)
    interest_rate = models.DecimalField(max_digits=5, decimal_places=2)
    loan_term = models.IntegerField()
    disbursement_date = models.DateField()

class LoanAdmin(admin.ModelAdmin):
list_display=('loan_id','customer_name','loan_amount','interest_rate','loan_term','disbursement_date')
```
![image](https://github.com/user-attachments/assets/5ab82380-746f-44f6-a7a6-882d04cc43a9)


# OUTPUT
![image](https://github.com/user-attachments/assets/66642ce2-2779-418a-9c5b-2a649ae97b87)
![image](https://github.com/user-attachments/assets/4cf96895-c994-42db-b627-e93e70079dcd)


# DEVELOPED BY : Gokul S
# REGISTER NO :212224240044

# RESULT
Thus the program for creating a database using ORM hass been executed successfully
