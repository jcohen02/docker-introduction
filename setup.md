---
title: Setup
---
### Website accounts to create
__\[?? Is this section still required??\]__

Please seek help at the start of the lesson if you have not been able to establish website accounts on both of:
- The [Docker Hub](http://hub.docker.com). We will use the Docker Hub to download pre-built container images, and for you to upload and download container images that you create, as explained in the relevant lesson episodes.
- [Bitbucket](http://bitbucket.org) is a code project repository site, akin to [GitHub](https://github.org). We will use Bitbucket to create a Docker container from a Docker image that you create.

### Software to install
Docker can be installed on Windows, Mac OS X and Linux platforms. However, in some circumstances, particularly on older operating system versions, installation can be challenging if you don't have a reasonable amount of technical knowledge and experience.

Workshop helpers will be on-hand to provide assistance if you're having problems getting Docker installed.

If you are unable to (or choose not to) install docker on your laptop, the workshop organisers may be able to provide access to a remote server with Docker pre-installed on which you can undertake this course.

Details of how to install Docker on different platforms are provided below:

- Microsoft Windows, either:
    - Try this first, although it won't work with Windows 10 Home Edition. Install the [Docker Desktop (Windows)](https://hub.docker.com/editions/community/docker-ce-desktop-windows), or failing that;
    - Install the [Docker Toolbox (Windows)](https://docs.docker.com/toolbox/toolbox_install_windows/).
- Apple MacOS, either:
    - Try this first, although it will not work with older versions of macOS. Install the [Docker Desktop (Mac)](https://hub.docker.com/editions/community/docker-ce-desktop-mac), or failing that:
    - Install the [Docker Toolbox (Mac)](https://docs.docker.com/toolbox/toolbox_install_mac/).
- Linux: Docker packages are provided for a number of Linux distributions: [CentOS](https://docs.docker.com/install/linux/docker-ce/centos/), [Debian](https://docs.docker.com/install/linux/docker-ce/debian/), [Fedora](https://docs.docker.com/install/linux/docker-ce/fedora/), [Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/). If you are running a different Linux distribution, see the details on [installing Docker Engine - Community from binaries](https://docs.docker.com/install/linux/docker-ce/binaries/).

### A quick tutorial on copy/pasting file contents from episodes of the lesson
Let's say you want to copy text off the lesson website and paste it into a file named `myfile` in the current working directory of a shell window. This can be achieved in many ways, depending on your laptop's operating system, but routes I have found work for me:
- macOS and Linux: you are likely to have the `nano` editor installed, which provides you with a very straightforward way to create such a file, just run `nano myfile`, then paste text into the shell window, and press <kbd>control</kbd>+<kbd>x</kbd> to exit: you will be prompted whether you want to save changes to the file, and you can type <kbd>y</kbd> to say "yes".
- Microsoft Windows running `cmd.exe` shells:
  - `del myfile` to remove `myfile` if it already existed;
  - `copy con myfile` to mean what's typed in your shell window is copied into `myfile`;
  - paste the text you want within `myfile` into the shell window;
  - type <kbd>control</kbd>+<kbd>z</kbd> and then press <kbd>enter</kbd> to finish copying content into `myfile` and return to your shell;
  - you can run the command `type myfile` to check the content of that file, as a double-check.
- Microsoft Windows running PowerShell:
  - The `cmd.exe` method probably works, but another is to paste your file contents into a so-called "here-string" between `@'` and `'@` as in this example that follows (the ">" is the prompt indicator):

        > @'
        Some hypothetical
        file content that is

        split over many

        lines.
        '@ | Set-Content myfile -encoding ascii

{% include links.md %}

{% comment %}
<!--  LocalWords:  myfile kbd links.md md endcomment
-->
{% endcomment %}
