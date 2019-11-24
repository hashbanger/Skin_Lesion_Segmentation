## Install virtualenv
Install virtualenv if you don’t already have it by typing pip install virtualenv at your terminal. Virtualenv allows you to create virtual environments for your app that house Python and all the dependencies your app requires. This includes specific version of plotly, dash, and other libraries that you know will work. 
As new updates become available, they won’t break your app until you’ve had a chance to test them first!


STEP 3 - Create a Development Folder
Create a new folder for your project. This will house the “development” copy of your app:
C:\>mkdir my_dash_app
C:\>cd my_dash_app


STEP 4 - Initialize Git
Initialize an empty git repository:
C:\my_dash_app>git init
Initialized empty Git repository in C:/my_dash_app/.git/

STEP 5 (WINDOWS) - Create, Activate and Populate a virtualenv
see below for macOS/Linux instructions!
Create a virtual environment. We’re calling ours “venv” but you can use any name you want:
C:\my_dash_app>python -m virtualenv venv
Activate the virtual environment:
C:\my_dash_app>.\venv\Scripts\activate 
Install dash and any desired dependencies into your virtual environment
(venv) C:\my_dash_app>pip install dash
(venv) C:\my_dash_app>pip install dash-auth
(venv) C:\my_dash_app>pip install dash-renderer
(venv) C:\my_dash_app>pip install dash-core-components
(venv) C:\my_dash_app>pip install dash-html-components
(venv) C:\my_dash_app>pip install plotly (requirement may be satisfied, see below)
At the time of this writing, pip install dash installs:
Flask-0.12.2 Jinja2-2.10 MarkupSafe-1.0 Werkzeug-0.14.1 certifi-2018.1.18 chardet-3.0.4 click-6.7 dash-0.21.0 decorator-4.2.1 flask-compress-1.4.0 idna-2.6 ipython-genutils-0.2.0 itsdangerous-0.24 jsonschema-2.6.0 jupyter-core-4.4.0 nbformat-4.4.0 plotly-2.5.1 pytz-2018.4 requests-2.18.4 six-1.11.0 traitlets-4.3.2 urllib3-1.22
Install a new dependency gunicorn for deploying the app:
(venv) C:\my_dash_app>pip install gunicorn


STEP 5 (macOS/Linux) - Create, Activate and Populate a virtualenv
Create a virtual environment. We’re calling ours “venv” but you can use any name you want:
$ python3 -m python3 -m virtualenv venv
Activate the virtual environment:
$ source venv/bin/activate
Install dash and any desired dependencies into your virtual environment
$ pip install dash
$ pip install dash-auth
$ pip install dash-renderer
$ pip install dash-core-components
$ pip install dash-html-components
$ pip install plotly (requirement may be satisfied, see above)
Install a new dependency gunicorn for deploying the app:
$ pip install gunicorn



STEP 6 - Add Files to the Development Folder
The following files need to be added:
app1.py	a Dash application
.gitignore	used by git, identifies files that won’t be pushed to production
Procfile	used for deployment
requirements.txt	describes your Python dependencies, can be created automatically
