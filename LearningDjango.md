create a new file and run this to create a vagrant file
```
vagrant init ubuntu/bionic64
```
Then changed Vagrant file with the script<br>
After doing this open a terminal from the folder and execute
```
vagrant up
```

to connect to vm
```
vagrant ssh
```
after connected
```
cd /vagrant
```
you will see the directory that is currently synchronized,Any changed made here will reflect in original folder<br>
How to run the code on vagrant server? Just like you run on normal machine
<br>
To create a new virtual python environment (in ssh)
```
python -m venv ~/env
source ~/env/bin/activate
deactivate
```
after activation install requirements.txt <br>
then,
```
django-admin.py startprojext profiles_project .
```
```
python manage.py startapp profiles_api
```
Now add these below into setting.py of **profiles_project**
```
'rest_framework',
'rest_framework.authtoken',
'profiles_api',
```
Now to check these changes, execute below command in ssh , vagrant folder
```
python manage.py runserver 0.0.0.0:8000
```
You can now search for below in browser
```
http://127.0.0.1:8000
```