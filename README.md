# Binary interaction parameters

Fitted **binary interaction parameters (k_ij)** for PC-SAFT / PCP-SAFT, covering binary pairs of CO2 and the impurities that occur in CO2 transport and storage streams.

Each pair directory contains the regression notebook, the reference data used for the fit, and the resulting parameters.

## Pairs covered

CO2 with Ar, CH4, CO, H2, H2S, N2 and O2 — plus cross pairs among the impurities themselves (`Ar_CH4`, `Ar_H2`, `Ar_N2`, `Ar_O2`, `CH4_H2`, `CH4_H2S`, `CO_Ar`, `CO_CH4`, `CO_H2`, `CO_H2S`, `CO_N2`, `H2_H2S`, `N2_CH4`, `N2_H2`, `N2_H2S`, `N2_O2`) and further combinations under `KIJ/other_impurities/`.

## Layout

- `KIJ/<PAIR>/` — one directory per binary pair: fitting notebook and results
- `KIJ/KIJ_matrix.ipynb` — assembles the full k_ij matrix
- `KIJ/parameters.json` — PCP-SAFT pure-component parameters
- `KIJ/BinaryInteractions.py` — regression routines
- `Experimental_data/` — reference VLE data used in the regressions

## Use with thermoift

This repository is consumed as a git submodule by [`thermoift`](https://github.com/Darz2/thermoift):

```bash
git clone --recurse-submodules https://github.com/Darz2/thermoift.git
```

## Citation

> Raju, D.; Skartlien, R.; Ramdin, M.; Vlugt, T. J. H. *Vapor–Liquid Interfacial Properties of CO2 Mixtures for Sequestration Applications: Molecular Simulations, Classical Density Functional Theory, and Equations of State.* Industrial & Engineering Chemistry Research (2026). https://doi.org/10.1021/acs.iecr.5c04932

## License

CC BY 4.0 — see [LICENSE](LICENSE). Experimental data collected from the literature remains subject to the terms of the original publications, which are cited in the corresponding notebooks.
