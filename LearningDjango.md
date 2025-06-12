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