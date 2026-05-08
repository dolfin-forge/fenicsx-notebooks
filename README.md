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

## Requirements

- FEniCSx 0.10.0
- Python 3.14
- conda / Miniforge

## License

MIT
