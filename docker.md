## DOCKER

## WHAT IS DOCKER?

Docker is an open platform for developing, shipping, and running applications.

Docker enables you to separate your applications from your infrastructure so you can deliver software quickly.

With Docker, you can manage your infrastructure in the same ways you manage your applications. 

By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.
 
 Docker is a software platform that allows you to build, test, and deploy applications quickly.

Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime.

Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.

##  How Docker works ?

Docker works by providing a standard way to run your code. Docker is an operating system for containers. 

Similar to how a virtual machine virtualizes (removes the need to directly manage) server hardware, containers virtualize the operating system of a server.

Docker is installed on each server and provides simple commands you can use to build, start, or stop containers.

![image](https://user-images.githubusercontent.com/119755263/207066629-5aa9870b-884c-48a6-88bd-337306a5a15b.png)

## WHAT IS DOCKER HUB ?

Docker Hub is a cloud-based repository in which Docker users and partners create, test, store and distribute container images. 

Through Docker Hub, a user can access public, open source image repositories, as well as use a space to create their own private repositories, automated build functions, webhooks and work groups.

Docker Hub is a registry service on the cloud that allows you to download Docker images that are built by other communities. 

You can also upload your own Docker built images to Docker hub.

![image](https://user-images.githubusercontent.com/119755263/207080246-31369143-0410-4f2d-8e0b-9c4fd09e054a.png)

## WHAT IS CONTAINER ?

Containers are used to Build, Share and Run your applications
 
A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. 

A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings. 

Container images become containers at runtime and in the case of Docker containers – images become containers when they run on Docker Engine.

Available for both Linux and Windows-based applications, containerized software will always run the same, regardless of the infrastructure.

Containers isolate software from its environment and ensure that it works uniformly despite differences for instance between development and staging. 

Docker containers that run on Docker Engine:

Standard: Docker created the industry standard for containers, so they could be portable anywhere

Lightweight: Containers share the machine’s OS system kernel and therefore do not require an OS per application, driving higher server efficiencies and reducing server and licensing costs

Secure: Applications are safer in containers and Docker provides the strongest default isolation capabilities in the industry

## TO INSTALL DOCKER USE THIS COMMAND BELOW :

  $ yum install docker

## Docker commands for creating a container for httpd :

# To start docker
 
  $ systemctl start docker

# To check the docker status 

  $ systemctl status docker
  
# To pull a httpd image from docker hub.

  $ docker pull httpd

# To list the images in docker
 
  $ docker image ls

# To start a container

  $ docker run -d --name myhttpd 8080:80 httpd
 
# To getting in to the running container
 
   $ docker container exec -it __containerid__ /bin/bash

# To list the container from outside the container
 
   $ docker container exec -it __containerid__ ls

  



