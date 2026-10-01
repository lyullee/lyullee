<div align="center">

# Ugwiyeon Lee (Lyul Lee)

### Chemical Engineering Software Developer

**Hydrogen safety systems, evidence-qualified scientific models, and reproducible research**

[![Python](https://img.shields.io/badge/Python-Scientific_Computing-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Domain](https://img.shields.io/badge/Domain-Hydrogen_Safety-0B7285?style=flat-square)](https://github.com/lyullee)
[![Focus](https://img.shields.io/badge/Focus-Reproducible_Research-2B8A3E?style=flat-square)](https://github.com/lyullee)
[![Repositories](https://img.shields.io/badge/Public_Projects-12-7048E8?style=flat-square)](https://github.com/lyullee?tab=repositories)

</div>

---

I develop scientific software at the intersection of **chemical engineering**, **process safety**, and **computational research**. My work spans operator-facing hydrogen-safety prototypes, document-grounded knowledge systems, atmospheric-dispersion models, source-term calculations, fire analysis, and atomistic materials research.

Across these projects, physical assumptions, evidence, validation status, and limitations are treated as part of the software—not as afterthoughts.

## Systems & decision support

| System | What it does | Status and scope |
|:--|:--|:--|
| [**hydrogen-station-sim**](https://github.com/lyullee/hydrogen-station-sim) | Physics-based hydrogen-refuelling-station digital twin with dynamic equipment models, 82 HAZOP sensor channels, faults, safety logic, consequence analysis, and 3D monitoring | Modelling, monitoring, and training prototype; not a certified controller |
| [**SAGA-PY**](https://github.com/lyullee/saga-py) | Python/FastAPI safety-knowledge assistant for Korean gas standards, law, and HAZOP analysis | Supports standalone document-grounded chat and dedicated digital-twin APIs; requires a lawful local corpus and provider credentials |
| [**SAGA-STS**](https://github.com/lyullee/saga-sts) | Earlier Java/Spring Boot edition of the SAGA gas-safety assistant | Preserved separately for reproducibility and further development; different runtime and APIs from SAGA-PY |

The digital twin and SAGA-PY are independent services that can work together: the simulator supplies calculated process and sensor context, while SAGA-PY provides an advisory knowledge layer. Neither replaces current regulations, site procedures, or qualified engineering judgment.

## Scientific model portfolio

### Dispersion and source terms

| Project | Purpose | Evidence boundary |
|:--|:--|:--|
| [**slabx**](https://github.com/lyullee/slabx) | Python reimplementation of the SLAB dense-gas dispersion model | Compared with the original Fortran and evaluated against 38 field and wind-tunnel trials |
| [**slabx-lh2**](https://github.com/lyullee/slabx-lh2) | Liquid-hydrogen extensions and an applicability diagnostic for SLABx | Seven-test, 210-record FFI research configuration with explicit routing limits |
| [**degadisx**](https://github.com/lyullee/degadisx) | Python reimplementation of EPA DEGADIS 2.1 | Retains the legacy thermodynamic and numerical route; deliberately excludes LH₂ research extensions |
| [**degali**](https://github.com/lyullee/degali) | Modern DEGADIS-based research model for cryogenic-hydrogen releases | Regression-tested compatibility path and an alpha-stage LH₂ extension with documented validation limits |
| [**lh2poolx**](https://github.com/lyullee/lh2poolx) | Evidence-qualified, quasi-steady LH₂ pool source term for a declared time window | Makes the release-to-ground and footprint assumptions explicit; not a dispersion or impact model |
| [**DynamicLH2PoolX**](https://github.com/lyullee/DynamicLH2PoolX) | Time-dependent LH₂ pool spreading, evaporation, inventory, and mass-balance model | Restricted Stage C component scope for declared ground inflow on horizontal surfaces |

### Fire, materials, and risk methods

| Project | Purpose | Reproducibility focus |
|:--|:--|:--|
| [**pifira**](https://github.com/lyullee/pifira) | Pressure-based inverse fire heat-flux and effective-area analysis, plus evidence-gated LH₂ thermodynamic utilities | Traceable LPG tank reconstruction and domain-checked LH₂ calculations |
| [**hydrogen-local-energetics**](https://github.com/lyullee/hydrogen-local-energetics) | Data and code for local hydrogen energetics and lattice-controlled mobility | Curated DFT records, archived ML-potential results, manifests, and figure-generation code |
| [**qsafety-qae**](https://github.com/lyullee/qsafety-qae) | Quantum amplitude-estimation research for safety and reliability probability models | Separates the probability model, classical baseline, circuit validation, and opt-in QPU execution |

## How the projects connect

```text
standards · law · HAZOP evidence
              │
              ▼
          SAGA-PY  ◄────────►  hydrogen-station-sim
          advisory layer       dynamic process + sensors

declared LH₂ release
      │
      ├── quasi-steady source ──► LH2PoolX
      └── dynamic ground pool ──► DynamicLH2PoolX

resolved source state
      │
      ├── SLAB family ──────────► slabx ──► slabx-lh2
      └── DEGADIS family ───────► degadisx / degali

fire exposure ─────────────────► pifira
material-scale behaviour ──────► hydrogen-local-energetics
risk-estimation methods ───────► qsafety-qae
```

The arrows describe intended information flow and research relationships, not universal model interchangeability or certification. Each repository documents its own coupling rules, validation domain, and conditions under which a result must be withheld.

## Engineering principles

```text
physical model  →  implementation  →  verification  →  validation
       ↑                                                   │
       └──────── limitations and reproducibility ◄─────────┘
```

I aim to make every important numerical result traceable: what assumptions produced it, where the model is valid, how it was checked, and how another researcher can reproduce it.

## Tools

`Python` · `FastAPI` · `NumPy` · `SciPy` · `pytest` · `CoolProp` · `Qiskit` · numerical modelling · scientific validation

## Use and citation

The repositories are open for inspection and reuse under their stated licences. For research use, consult each project's `CITATION.cff`, documentation, validation record, data policy, and limitations before applying its results. Safety-related outputs are research or decision-support artefacts unless a repository explicitly states otherwise.

<div align="center">

[All repositories](https://github.com/lyullee?tab=repositories) · [SLABx documentation](https://github.com/lyullee/slabx#documentation) · [SAGA-PY](https://github.com/lyullee/saga-py) · [Hydrogen station simulator](https://github.com/lyullee/hydrogen-station-sim)

</div>
