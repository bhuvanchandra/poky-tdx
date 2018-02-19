Yocto Poky Setup
===================

Install the repo bootstrap binary:
```
$  mkdir ~/bin
$  PATH=~/bin:$PATH
$  curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
$  chmod a+x ~/bin/repo
```

Or

One can install `repo` tool via respective distro feeds.

e.g.:

On Arch Linux:
```
# pacman -S repo
```

On Ubuntu:
```
# apt-get install repo

```

After installing `repo` tool, create a directory for your yocto build setup to live in and clone the meta information.
```
$ mkdir ${HOME}/yocto
$ cd yocto
$ repo init -u http://github.com/bhuvanchandra/yocto-poky.git -b master
$ repo sync
```

Note:
Optionally create a development branch in all git repositories
```
$ repo start devel --all
```
After successful `repo sync`, once an see the below directory structure:

```
yocto
├── export
└── layers
```
`layers` directory contains all the required meta layers

`export` script will initialize the bitbake env

After sourcing the `export` script one can start building image/s

```
$ source ./export
$ echo ${PWD}
$ /home/dvb/yocto/build
$ MACHINE=raspberrypi bitbake -k core-image-minimal
...
```

