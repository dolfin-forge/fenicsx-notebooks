# FEniCSx Notebooks

Teaching and demo notebooks for FEniCSx 0.10.0.

Part of the [dolfin-forge](https://github.com/dolfin-forge) project.

## Setup

```bash
conda create -n fenicsx -c conda-forge fenics-dolfinx mpich pyvista matplotlib jupyter
conda activate fenicsx
jupyter lab
```

## Notebooks

| Notebook | Description |
|---|---|
| `poisson.ipynb` | Poisson equation, P1 elements, exact solution verification |
| `stokes.ipynb` | Stokes lid-driven cavity, Taylor-Hood P2/P1 elements |
| `navier-stokes.ipynb` | Navier-Stokes lid-driven cavity, backward Euler, Taylor-Hood P2/P1, Re=100 |

## Notes on the Navier-Stokes solver

The time loop uses MUMPS for sparse LU factorization. On Apple Silicon (M-series Macs), MUMPS uses OpenMP threading which can cause non-deterministic floating-point results. The notebook sets `OMP_NUM_THREADS=1` and raises the MUMPS pivot threshold `CNTL(1)=0.1` to ensure stable results. See commit `1686ac2` for the full diagnosis.

## Requirements

- FEniCSx 0.10.0
- Python 3.14
- conda / Miniforge

## License

MIT
