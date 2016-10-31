## To build(from the directory this file is in):

```
source environment
mkdir build
cd build
cmake $CUSTOM_CMAKE_FLAGS ../CUF
make
```

## To run(Assuming MPS has been enabled):
```
mpirun -gpu -n 16 --map-by ppr:16:node Collective
```
