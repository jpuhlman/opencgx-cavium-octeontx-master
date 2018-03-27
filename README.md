# Release repository for cavium-thunderx

Montavista Software, LLC. release of cavium-thunderx. 

How to use:
==========

```
git clone --recursive https://github.com/MontaVista-OpenSourceTechnology/opencgx-cavium-thunderx-4.14-2.4
cd opencgx-cavium-thunderx-4.14-2.4
source setup.sh
```
By default, the script will create a project called project, you may change this
by adding the directory name you would like to use on the source line:

```
source setup.sh <my directory>
```

After running the top level setup.sh, you are ready to build. When starting
another session, you can source the setup.sh script in the project directory
to get started. This script will automatically source the environment for
the build tools stored under buildtools, and sources the 
poky/oe-init-build-env script.

From that point, the project should work like any other yocto based build system. So
a command like the following will build images that you can run via qemu or on a real target.

```
cd project
or
cd <my directory>
source setup.sh
bitbake core-image-minimal 
runqemu cavium-thunderx nographic slirp
```

For additional information see the yocto documentaion: https://www.yoctoproject.org/docs/

directory layout:
================
```
opencgx-cavium-thunderx-4.14-2.4/
       project - bitbake project for the cavium-thunderx project build
       buildtools - build tools to provide minimal build requirement for poky builds
       layers - layers for building cavium-thunderx project
       setup.sh - project setup script  
```
