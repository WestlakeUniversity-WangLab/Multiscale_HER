# Microkinetic Modeling (MKM)

This repository contains the microkinetic modeling framework and input files to reproduce the multiscale simulations in the article "Toward Rational Understanding of the Hydrogen Evolution Polarization Curves Through Integrating Ab Initio Simulations and Mass Transport Effects". The implementation couples grand canonical density functional theory (GC-DFT) calculations with continuum transport modeling through iterative parameter updates, enabling prediction of HER polarization behavior across the full pH range.

## Overview

This directory contains all input files required to performe the microkinetic modeling simulations. 

The microkinetic simulations were performed using the **MKMCore** open-source computational framework.

Core Framework
Complete MKM source code is available in the main repository:
https://github.com/WestlakeUniversity-WangLab/MKMCore/

This work implements iterative coupling between continuum transport model and MKM:

1. **Initial Input**: Bulk pH and H₂ concentration as MKM initial conditions
2. **MKM Calculation**: Current density and reaction rates
3. **Continuum Calculation**: Local pH and H₂ concentration
4. **Parameter Update**: Feed updated parameters back to MKM
5. **Iteration Convergence**: Repeat until parameters converge
Key coupling parameters in base_config.json:

Key coupling parameters in `base_config.json`:

```json
{
    "thermo": {
        "pH": "local_pH_from_continuum_model"
    },
    "species": {
        "H2_aq": {
            "concentration": "local_H2_concentration_from_continuum_model"
        },
        "OH:-_aq": {
            "concentration": "10^(-14+local_pH)"
        },
        "H3O:+_aq": {
            "concentration": "10^(-local_pH)"
        }
    }
}
```



## Input Files

### Example Input Files (pH = 1)

All example input files are provided for pH = 1 conditions:

- **HER_0ML.jmkm**: Configuration for zero hydrogen coverage (θ_H = 0 ML)

- **HER_HML.jmkm**: Configuration for high hydrogen coverage (θ_H = 7/9 ML）

## Technical Details

- **Convergence**: Local concentration of all species change < 1%

- **Strategy**: Relaxation iteration for numerical stability

- **Data Transfer**: JSON configuration and CSV data files


## Configuration Notes

- **Output Path**: The writer uses relative path `./output_files/output.csv` for better portability

- **Solver Stability**:  For convergence issues, `NullGuesser` can be replaced with `ODEGuesser` to improve solver stability

