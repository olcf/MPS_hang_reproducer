## To build(from the directory this file is in):

```
$ source environment
$ mkdir build
$ cd build
$ cmake $CUSTOM_CMAKE_FLAGS ../CUF
$ make
```

## To run(MPS must be enabled):
```
$ mpirun -gpu -n 2 --map-by ppr:2:node ./Collective
```
