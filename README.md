# ML-meets-Docker
MLOPs concept of using &amp; utilizing the power of containzeration using Dockers

### Understanding the core idea
Dockerfile is a script file which is run to build a docker image. <br>
Running a docker image creates docker containers. <br>
DockerFile -> Docker Image -> Docker Containers <br><br><br>

#### Common commands for Docker
Common commands used while writing a DockerFile <br><br><br>
 * FROM
 * COPY
 * ENV
 * RUN 
 * CMD
 * ENTRYPOINT

FROM command is useful when your codebase has a lot of dependencies. It is wise to use a pre-built image which has those **dependencies pre-installed** rather than installing one by one using RUN pip install package. <br><br>
COPY command as the name states, used to copy. :) <br><br>
ENV command is used to declare variable names which can be either used as user inputs or can be directly defined in the dockerfile to be used as os.environment['name'] in the scripts (if python) <br><br>
RUN command is used to run a specific instruction. Usually a shell command you would execute to **build a docker image** and commit those changes permanently (until you make changes and update). <br><br>
CMD command are the default commands which the container would execute when you invoke a docker image. However, the CMD can be overridden by passing the arguments while docker run $image.<br><br>
ENTRYPOINT command is used to modify the way a container starts. I'm yet to discover more about this. Will update the repo when I do so.<br>

<br><br>
Before we begin, let's talk about what the idea of dockers is. Rather than making a linux VM and installing all dependecies, docker is a isolated system which doesn't require another OS to work. That means, lighter faster but Command Line Interface majorly (without porting).


### Creating a Docker Image
Steps to create your docker image & run docker containers for ML projects. <br><br>
 - Create the necessary scripts which you'd like to dockerize.
 - Create your Dockerfile
 - Build your dockerfile with appropriate set of commands (we'll get to building of docker image at a later stage)



## Pushing docker images to Dockerhub
You'd like your docker image to be used by others if the project isn't private. <br>
Pushing a docker image is as simple as push as git repo code. <br>
docker push <image-name>:<tag-if-any>
