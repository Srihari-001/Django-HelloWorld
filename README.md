# Django-HelloWorld
Run Hello World program in Django using Pycharm

Today I thought of creating a demo python project. so I choose "Hello World" program.

**Aim:**
To create a Hello World Project in Python using Django.

**Why:**
I need to master DevOps skills so I thought is satrting by writing very basic and small projects and get hands on exp on them.

How:

**step01**: _Integrate Django in Pycharm Community Edition_

   I folllowed a youtube video (link : https://youtu.be/WluSpfSMj2Y?si=lVQPUqytRmMWSGeL), thru this i completed the integration step
    
  -> create a new project in pycharm and give its name as "project01".
    
  -> Open the terminal in main.py dir,choose git bash and provide the below cmd,

      pip install django
    
  -> Now delete the main.py file in project01 folder.

  -> Again open bash terminal anf provide the below cmd to create the project name,

    django-admin startproject project001

  -> make sure manage.py file and project001 folders are in project01 dir. as shown in figure ![image](https://github.com/Srihari-001/Django-HelloWorld/assets/118358492/0e03c52b-c016-4f2d-9688-1baf78761ffc)

  -> Now open bash terminal and provide below cmd to create app.

    python manage.py startapp helloworld 
  
  or
    
    django-admin startapp hellowworld

  -> Now click "Edit Run Configuration" and delete the main and click + to create Django file.
  -> provide name as "Django"
  -> scrpit path as "manage.py" file path in projects.
  -> give parameters:runserver
  -> Working Directory:"project01" path
  -> intrepreter:python
  -> click Apply and OK.

  ->**Run Django.py file**

  -> browse the http link : http://127.0.0.1:8000/
  -> You can view the Dajngo Server welcome page.

  **Step02**: _Create Hello World Program_

  -> Navigate to the directory where manage.py is located using the terminal inside PyCharm or an external terminal.

    python manage.py startapp helloworld

  -> Within the helloworld app directory, you'll see a views.py file. Open it and define a simple view:

    from django.http import HttpResponse

    def hello(request):
        return HttpResponse("Hello, World!")

  -> First, within the helloworld directory, create a new file named "**urls.py**". In helloworld/urls.py, add:

    from django.urls import path
    from . import views

    urlpatterns = [ path('', views.hello, name='hello'),]

  -> you'll need to include this in the project's main urls.py, which can be found in the myproject directory (or whatever name you gave to your project). Modify 
     myproject/urls.py to look like

       from django.contrib import admin
       from django.urls import path, include
        
       urlpatterns = [
            path('admin/', admin.site.urls),
            path('helloworld/', include('helloworld.urls')),
            path('', include('helloworld.urls')),  # Add this line
        ]

  -> Open a web browser and navigate to " http://127.0.0.1:8000 ". You should see "Hello, World!" displayed.
  
  

  
  
  

