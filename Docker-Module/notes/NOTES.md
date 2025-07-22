What are containers?

- A lightweight portable units for running applications 

- They bond an application with all its dependencies ensuring it runs consistently across different environments

For example:

I want to run every part of the application, containers will include the code, the runtime, libraries, and anything I need including the application needs to run and because it is isolated, it runs the same on any environment.

You have three containers that sits above a docker engine, each container has the app and its binary and the libraries that the app requires to run and docket engine sits in line with host operating system and the docker engine sits in line with the host operating system and that sits ontop of on instrafracture.

Benefits of Containers:

- Each container is isolated from underlying system
- Ensures application runs smoother without interferences
- Containers provide a consisteny environment for applications to run
- Makes development and development more reliable

What is Docker?

- Open platform for developing, shipping and running applications in containers
- It simplifies the process of managing containers making it easier to build, deploy and run applications

Difference between images and containers:

-   Images are templates that create containers, like a snapshot of the application at a certain point of time, they don't change once they are created, the immunitability ensures the applications runs consistently no matter where its deployed.

- Containers are running instances of images, images are snapshot of the application, containers are running instances of these images.

Example: If an image is a recipe, the containers are the dishes you create from the recipe, i.e the image. It's the thing you interact with, you can start, stop and modify as needed.

We create these images via docker file, a file to build docker images, it contains a series of images that docker uses to assemble an image. Like what image to use, what files to copy to the container and what commands to run in the container.

Docker in summary is an essential tool for modern software development and operations, it simplifies the process, creating, deploying and managing containers.


Key components of Docker:
1. Docker engine - core service that runs containers
2. Docker hub - a repo where you can find and share, like  app store
3. Docker compose - manages more than one of these containers, it's like writing a recipe for how your entire app should run, docker compose helps you orchesstrate components together.
4. Images are templates for creating containers, like a snapshot of an application
5. Docker file - a file to build docker images from a set of instructions


Containers vs. Virtual Machine

- A VM allows multiple operating systems to run on a single server machine




