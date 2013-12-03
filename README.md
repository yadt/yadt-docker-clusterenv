yadt-docker-clusterenv
======================

develop yadt components while they run in a docker cluster simultaneously

Prerequisites
-------------

* [docker](https://www.docker.io/): *an open source project to pack, ship and run any application as a lightweight container*
    * You MUST be able to use docker as [non-root user](http://docs.docker.io/en/latest/use/basics/#why-sudo)
* [bash](http://www.gnu.org/software/bash/)
* [python](http://www.python.org/)
* [docopt](http://docopt.org/)
* [docker-clusterenv](https://github.com/arnehilmann/docker-clusterenv.git)


tl;dr: initialization (just once)
---------------------------------

```bash
git clone https://github.com/arnehilmann/docker-clusterenv.git
cd docker-clusterenv
./build-images
cd ..

git clone https://github.com/yadt/yadt-docker-clusterenv.git
cd yadt-docker-clusterenv

git submodule init
git submodule update
```

tl;dr: normal usage
-------------------

```bash
./start-minion foo1
./start-minion foo2
./start-shell master

# on 'master'
ssh foo1 hostname

yadtshell status

# ...

# to stop the whole cluster
/local-fs/out/stop-clusterenv
exit
```

TODO/Coming Soon
----------------

* create target file automatically
* integrate more yadt components
* pimp bash prompt of machines, to know where you are

* [TODOS of docker-clusterenv](https://github.com/arnehilmann/docker-clusterenv#todo)

