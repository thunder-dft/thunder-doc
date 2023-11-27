# Installation

## Installation of FIREBALL

* Intel compiler (MKL, ifort, icc, mpi)
* Clone [thunder-master]() and [thunder-fireball]()
* Edit `src/include/OPTIONS`, `src/MACHINE/MYMACHINE`, `src/Makefile`
* Run `make fireball-ase.x`

## Installation of thunder-ase

`thunder-ase` package is not only the ASE interface for FIREBALL, but also provides many other useful functions. 

* Just Run `pip install -U thunder-ase` in terminal. That's all.

**Requirements**

* ase
* dftd4 and dftd4-python for DFT-D4 (optional)