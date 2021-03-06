---
title: "Introducing the Docker command line"
teaching: 10
exercises: 0
questions:
- "How do I interact with Docker?"
objectives:
- "Explain how to check that Docker is installed and is ready to use."
- "Demonstrate some initial Docker command line interactions."
keypoints:
- "A toolbar icon indicates that Docker is ready to use containers."
- "You will typically interact with Docker using the command line."
---
### Docker command line

Start the Docker application that you installed in working through the setup instructions for this session. Note that this might not be necessary if your laptop is running Linux. 

The Docker application will usually provide a way for you to log in using the application's menu (macOS) or systray icon (Windows). This will require you to use your Docker Hub username and your password.

> ## Determining your Docker Hub username
> If you no longer recall your Docker Hub username, e.g., because you have been logging into the Docker Hub using your email address, you can find out what it is through the steps:
> - Open <http://hub.docker.com/> in a web browser window
> - Sign-in using your email and password (don't tell us what it is)
> - In the top-right of the screen you will see your username. Mine's `dme26`.
{: .callout}

Now open a shell window, and run the following command in your shell to check that Docker is installed. I have appended the output that I see on my Mac, but the specific version is unlikely to matter much: it certainly does not have to precisely match mine.
~~~
$ docker --version
~~~
{: .language-bash}
~~~
Docker version 18.09.1, build 4c52b90
~~~
{: .output}

Ensure that your command line `docker` commands are able to reach the Docker Hub by running the following command:
~~~
$ docker login
~~~
{: .language-bash}
~~~
Authenticating with existing credentials...
Login Succeeded
~~~
{: .output}
(I wasn't prompted for authentication details, if you are, then you need to use your Docker Hub username and password.)

The `Login Succeeded` message means that your `docker` command line tool is ready to access the Docker Hub. We will return to discussion of the Docker Hub soon...

The above commands have not actually relied on the part of Docker that runs lightweight virtual machines being operational. Somewhat stretching a physical analogy, you can think of the above Docker commands having been instructions to the cranes on a hypothetical shipping dock, but we haven't actually checked if the container ship we want to interact with is present yet. A command that checks that the virtual machine host is running is the Docker process list command, which we cover in a later episode.

Without explaining the details, output on a newly installed system would likely be:
~~~
$ docker ps
~~~
{: .language-bash}
~~~
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
~~~
{: .output}
(The command `docker info` will achieve a similar end. but produces potentially daunting volumes of output.)

However, if you instead get a message similar to the following
~~~
Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?
~~~
{: .output}
then you need to check that you have started the Docker Desktop, Docker Engine, or however else you worked through the setup instructions.


{% include links.md %}

{% comment %}
<!--  LocalWords:  keypoints links.md endcomment systray
 -->
{% endcomment %}
