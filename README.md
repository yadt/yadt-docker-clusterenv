yadt-docker-clusterenv
======================

develop yadt components while they run in a docker cluster simultaneously


tl;dr
-----

```bash
git clone https://github.com/yadt/yadt-docker-clusterenv.git
git clone https://github.com/arnehilmann/docker-clusterenv.git

cd yadt-docker-clusterenv

git submodule init
git submodule update

./start-minion foo1
./start-minion foo2
./start-shell master

# on 'master'
ssh foo1 hostname
```

TODO/Coming Soon
----------------

* create target file automatically
* integrate more yadt components

