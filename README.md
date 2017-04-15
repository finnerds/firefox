# firefox

Firefox in a Container

Docker provides in the meantime support for multiple (non linux) operating systems. Why not isolate the applications in individual containers and run all applications within a container. This way you dont need to look after setups and conflicts between versions, as every poor windows user has for centuries now. Even Windows10 runs by now within Docker, so have fun with the different repositories which enable you to run applications in a container and make you a tiny bit more independent from the majors and improve your security.

To make use, simply type in

    $ docker pull finnerds/firefox
    $ docker run -ti --rm \
       -e DISPLAY=$DISPLAY \
       -v /tmp/.X11-unix:/tmp/.X11-unix \
       finnerds/firefox
       
If you like to read more about this and other solutions, please checkout the following links

* https://blog.bennycornelissen.nl/bwc-gui-apps-in-docker-on-osx/
* http://fabiorehm.com/blog/2014/09/11/running-gui-apps-with-docker/
* https://github.com/sameersbn/docker-browser-box
