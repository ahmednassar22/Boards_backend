# Render Bootstrap
<ol>
	<li>nside shell
		<ol>
			<li>Download environment
				<ol>
					<li>virtualenv venv</li>
				</ol>
			</li>
			<li>activate environment:
				<ol>
					<li>venv\Scripts\activate</li>
				</ol>
			</li>
			<li>download django:
				<ol>
					<li>pip install django</li>
				</ol>
			</li>
			<li>download django rest framework
				<ol>
					<li>pip install djangorestframework</li>
				</ol>
			</li>
			<li>create the project:
				<ol>
					<li>django-admin startproject discussion_doard .</li>
				</ol>
			</li>
<li>create the app:
	<ol>
		<li>python.exe manage.py startapp boards</li>
		</ol>
			</li>
		</ol>
	</li>
	<li>inside settings file from discussion_board folder add inside INSTALLED_APPS list:
		<ol>
			<li>‘boards’,</li>
			<li>‘rest_framework’,<li>
		</ol>
	</li>
</ol>
	
