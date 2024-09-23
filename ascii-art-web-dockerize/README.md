# ASCII Art Web Dockerize

## Overview
Ascii Art Web dockerize is a golang web application that converts an input text to generate an ASCII via web browser based on the three banner files provided in this project.

The project further utilized docker image and engine to run the project based on a docker file to create a docker image to run the project.

## Installation
To use ASCII Art Web dockerize , you'll need Go installed on your system. You can install it via the official Go website.

Clone the repository:
```
git clone https://learn.zone01kisumu.ke/git/svictor/ascii-art-web-dockerize
```
## Usage

1.Building the docker image
```
docker build . -t ascii-art-web-dockerize
```
 Means to build a docker container based on the docker configuration in the current directory.

-t means tag or the name we've given the container supposed to be built.

2.Running the container
```
docker run  -d -p 4000:8082  --name  newdesign ascii-art-web-dockerize 
```

-p 80:8080: Maps port 4000 on your computer to port 8080 inside the container.

ascii-art-web-dockerize:latest: Uses the specified Docker image (with the latest version) to create the container.

3.Open your prefered browser and enter http://localhost:8082 to view the application

## Cleaning up
We  have alternatively added a bash script named cleaner.sh that will help to cleanup the created docker containers  to automate the process.

```
sh cleaner.sh

```
Finally we have also included a .dockerignorefile that will help reduce context size by excluding unnecessary files and directories hence builds time faster and less data transfer.

## Contributing
Contributions are welcome! If you have suggestions for improvements, please open an issue or create a pull request on the GitHub repository.


## Contributers
* [svictor](https://learn.zone01kisumu.ke/git/svictor)
* [bobaigwa](https://learn.zone01kisumu.ke/git/bobaigwa)
