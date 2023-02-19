# Boards_backend
<ul>
 <ol>## Inside shell
	 <ol>### Download environment
#### <li>i.virtualenv venv
	</li></ol>
### b.	activate environment:
#### i.	venv\Scripts\activate
c.	download django:
i.	pip install django
d.	download django rest framework
i.	pip install djangorestframework
e.	create the project:
i.	django-admin startproject discussion_doard .
f.	create the app:
i.	python.exe manage.py startapp boards
	</ol>
2-	inside settings file from discussion_board folder add inside INSTALLED_APPS list:
a.	‘boards’,
b.	‘rest_framework’,
3-	Create models:
a.	Inside models file from boards folder 
i.	Copy models file from boards folder from old project and pest it
4-	Create data base:
a.	Inside settings file from discussion_board folder 
i.	Copy database from settings file from discussion_board folder from old project and pest it and modified the name of database
5-	Do make migration
a.	Inside shell :
i.	ython.exe manage.py makemigrations
ii.	python.exe manage.py migrate
6-	register for models
a.	inside admin file from boards folder add:
i.	from .models import *
ii.	admin.site.register(Board)
7-	create super user:
a.	inside shell:
i.	python.exe manage.py createsuperuser
8-	create views in backend:
a.	inside views file from boards folder:
i.	from .models import *
ii.	from django.http import JsonResponse
iii.	def boards_list(request):
boards = Board.objects.all()
data = {‘Results’:list(boards.values(“pk”,”name”,”description”))}
return JsonResponse(date)
b.	def board_topic(request,board_id):
board = get_object_or_404(Board,pk=board_id)
data = {“results”:{
	“name”:board.name,
	“description”:board.description
	}}
Return JsonResponse(data)
c.	
9-	Create url:
a.	Inside boards folder create url file type py:
i.	Copy url file from boards folder from old project and pest it
ii.	
10-	Connection url project whit url app:
a.	From djang.urls import path,include
b.	Inside urlpatterns add:
i.	Path(‘’,include(‘boards.urls’))
</ul>
