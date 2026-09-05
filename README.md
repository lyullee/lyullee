<div align="center">

# Ugwiyeon Lee (Lyul Lee)

### Chemical Engineering Software Developer

**Open, reproducible tools for hydrogen safety, dispersion modelling,**  
**fire analysis, and materials energetics**

[![Python](https://img.shields.io/badge/Python-Scientific_Computing-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Domain](https://img.shields.io/badge/Domain-Hydrogen_Safety-0B7285?style=flat-square)](https://github.com/lyullee)
[![Focus](https://img.shields.io/badge/Focus-Reproducible_Research-2B8A3E?style=flat-square)](https://github.com/lyullee)
[![License](https://img.shields.io/badge/Projects-MIT-7048E8?style=flat-square)](https://github.com/lyullee?tab=repositories)

</div>

---

I develop scientific software at the intersection of **chemical engineering**, **process safety**, and **computational research**. My work turns physical models and experimental evidence into transparent Python tools—with validation, limitations, and reproducibility treated as part of the software itself.

## Research & engineering focus

- Atmospheric dispersion of dense and cryogenic gases
- Liquid-hydrogen release and safety-distance assessment
- Inverse analysis of fire heat flux from vessel pressure histories
- Local hydrogen energetics and lattice-controlled mobility
- Model verification, validation, uncertainty, and reproducible computation

## Featured work

| Project | Purpose | Evidence & reproducibility |
|:--|:--|:--|
| [**slabx**](https://github.com/lyullee/slabx) | Python reimplementation of the SLAB dense-gas dispersion model | Compared with the original Fortran and evaluated against 38 field and wind-tunnel trials |
| [**slabx-lh2**](https://github.com/lyullee/slabx-lh2) | Liquid-hydrogen extensions and an applicability criterion for SLAB | Includes cryogenic-water physics, diagnostics, and conditions for 35 trials |
| [**pifira**](https://github.com/lyullee/pifira) | Pressure-based inverse fire heat-flux and effective-area analysis for LPG and LH₂ tanks | Reconstructs thermal exposure from pressure histories |
| [**hydrogen-local-energetics**](https://github.com/lyullee/hydrogen-local-energetics) | Reproducibility data and code for local hydrogen energetics | Connects local energetics with lattice-controlled mobility |

## How the projects connect

```text
release scenario
      │
      ├── atmospheric dispersion ──► slabx ──► slabx-lh2
      │
      ├── external fire exposure ──► pifira
      │
      └── material-scale behaviour ─► hydrogen-local-energetics
```

## Engineering principles

```text
physical model  →  implementation  →  verification  →  validation
       ↑                                                   │
       └──────── limitations and reproducibility ◄─────────┘
```

I aim to make every important numerical result traceable: what assumptions produced it, where the model is valid, how it was checked, and how another researcher can reproduce it.

## Tools

`Python` · `NumPy` · `SciPy` · `pytest` · `CoolProp` · numerical modelling · scientific validation

## Use and citation

The repositories are open for inspection and reuse under their stated licences. For research use, please consult each project's `CITATION.cff`, documentation, validation record, and limitations before applying its results.

<div align="center">

[Repositories](https://github.com/lyullee?tab=repositories) · [slabx documentation](https://github.com/lyullee/slabx#documentation) · [slabx citation](https://doi.org/10.5281/zenodo.22023625)

</div>
