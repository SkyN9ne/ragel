# Ragel State Machine Compiler


### DEPENDENCIES
============

```Ragel``` depends on the ```Colm``` Programming Language. For now, the two packages move
in close lockstep. If building ```ragel``` from source, generally, the ```master``` branch of
```colm``` is required. For releases, the specific version of ```colm``` needed is in
```EXPECTED_COLM_VER``` in ```configure.ac```

## BUILDING
========

Ragel is built with ```autotools```. If building from revision control you need to
run ```autogen.sh```
Then you can run and use ```configure``` and ```make```
In a ```Bash``` shell for example:

```bash
./autogen.sh
./configure --prefix=$PREFIX --with-colm=$COLM_INSTALL_PATH
make
```

There are three ```Dockerfile```'s that demonstrate installing dependencies and
building:

- ```full.Dockerfile``` installs all dependencies, including testing dependencies,
  builds ```master```, and does full testing.

- ```master.Dockerfile``` does a basic build from ```master``` without testing.

- ```release.Dockerfile``` builds and installs the ```release``` build ```tar```balls

