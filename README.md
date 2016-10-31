To build(from the directory this file is in):

source environment
mkdir build
cd build
cmake $CUSTOM_CMAKE_FLAGS ../CUF
make

To run:
# enable MPS: this is down through the bsub app GPUMPS on summitdev.ccs.ornl.gov
mpirun -gpu -n 16 --map-by ppr:16:node Collective
