Docker container for Python Flask slideshow. Elastic Beanstalk auto-scales this container.

- docker-amazon: official amazon eb python container 
	- ubuntu
	- uwsgi
	- python

- docker-centos: official centos 6.5 latest
	- centos 6.5.3
	- gunicorn 19.3.0
	- python 2.7.9
	

```
==> docker run -d -p 8011:8011 $(docker build . | tail -1 | awk '{print $NF}')
```

notes:

- docker on linux requires "docker" group membership for user
- docker on osx requires boot2docker and helper script for port redirection
	- sudo boot2docker init
	- sudo boot2docker run
	- sudo boot2docker ssh -vnNTL 8011:localhost:8011
