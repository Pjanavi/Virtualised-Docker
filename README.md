 Set Up a Virtualized Environment Using Docker
 -
 In this project we'll create a Docker container using a base image (Ubuntu) and (python) and install necessary software  to run a simple Python (Hello world) application. This demonstrates how Docker containers are used to encapsulate software environments and managing virtualized applications.

 1> To install "DOCKER DESKTOP" from docker official website an download the installer for windows.
 
     -->Run the installer, and select WSL.
     
     -->login into your google account and ensure that the docker is running.

 2> Open Windows powershell (run as administrator) and install wsl:

      --> wsl --install

 3> In doctor desktop --> "Container" search for "ubuntu"(official image) and hello-world and click on run and download. this will download ubuntu image in your docker account. 

 4> To verify your installation of docker, go to the powershell terminal and run "docker --version" to verify installation and try runnign the hello-world container by using "docker run hello-world".

 Setting up a dockerized environment through powershell 
 -
 
 --> docker pull ubuntu (this will pull your ubuntu base image from your docker hub)
 
 By this feature we can know that dockers has the ability to create isolated environment.

 Installing a software and its requirements inside a docker for running a simple web application(Hello world):
 -
 
install python software in docker by searching in the containers page "python"

Now we are installing another container just like we did for ubuntu called "python" from the docker hub

it will automatically install the python version suitable in your laptop 3.13.1

 mkdir flask-docker-app 
 
 cd flask-docker-app

 NOW LETS ADD A BASIC PRINTING CODE OF HELLO WORLD:
 
 from fastapi import FastAPI

app = FastAPI()


@app.get("/")

async def root():

    return {"message": "Hello World"}

    

--> and execute the following commands on your docker terminal in the respective folder

C:\Users\janav\flask-docker-app>docker init

? What version of Python do you want to use? 3.13.1

? What port do you want your app to listen on? (8000)


check your flask-docker-app directory, it should include app.py, requirements.txt, dockerfile. .gitignore, READMe, compose.yaml

for running the application on a virtualized environment use the following command 
--

docker compose up --build

This will print the output of your application locally on:

https://localhost:8000

Output
-- 

    {
         "message": "Hello World" 
          }

     
