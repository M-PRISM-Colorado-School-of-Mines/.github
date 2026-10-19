<div align="center">

<img src="https://raw.githubusercontent.com/M-PRISM-Colorado-School-of-Mines/.github/main/profile/banner.svg" alt="M-PRISM at the Colorado School of Mines: fast, accurate, open reactor physics" width="100%"/>

### ⚛️ Fast, accurate, open reactor physics, from fission matrices to digital twins

[![Colorado School of Mines](https://img.shields.io/badge/Colorado_School_of_Mines-002554?style=for-the-badge&logoColor=white)](https://www.mines.edu)
[![OpenMC](https://img.shields.io/badge/OpenMC-0a6ebd?style=for-the-badge&logo=python&logoColor=white)](https://openmc.org)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org)
[![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)](https://isocpp.org)
[![Website](https://img.shields.io/badge/vmascolino.com-00b4d8?style=for-the-badge&logo=googlechrome&logoColor=white)](https://www.vmascolino.com)

</div>

---

## 🌟 Who we are

**M-PRISM** is the Reactor Physics Group at the **Colorado School of Mines**, led by [Valerio Mascolino](https://www.vmascolino.com). We develop the computational tools that let reactor designers, regulators and operators get **Monte Carlo accuracy at a fraction of the cost**: validated against real experiments, built on open-source software, and aimed at the next generation of research, advanced and space reactors.

<table>
<tr>
<td align="center" width="25%"><h3>⚡ 10²–10⁴×</h3><sub>typical speed-up of fission-matrix transport over direct Monte Carlo¹</sub></td>
<td align="center" width="25%"><h3>🧪 Experiment-first</h3><sub>validated on measured data from the JSI TRIGA Mark-II, not just code-to-code</sub></td>
<td align="center" width="25%"><h3>🔓 Open by design</h3><sub>OpenMC, Python and C++, with public model libraries</sub></td>
<td align="center" width="25%"><h3>🌍 Collaborative</h3><sub>JSI Ljubljana · Politecnico di Milano · Virginia Tech heritage</sub></td>
</tr>
</table>

<sub>¹ Reported for the RAPID code system across its validation benchmarks (pre-calculation of the coefficient database excluded).</sub>

---

## 🔬 What we work on

| | Focus | In a sentence |
|---|---|---|
| 🧮 | **Fission Matrix & Transient Fission Matrix** | Recast neutron transport as a linear eigenvalue problem, so criticality, 3-D flux and full time-dependent kinetics solve in seconds, with no source-convergence headaches. |
| 🛠️ | **Open-source tooling for OpenMC** | Bringing fission-matrix and kinetics capability to the much larger OpenMC community. |
| 📚 | **Open reactor model library** | A growing, documented set of OpenMC reactor models that others can run, verify and extend. |
| 🎯 | **Experimental validation** | Control-rod worth, dosimetry, burnup and kinetics measured at the JSI TRIGA Mark-II (Ljubljana). |
| 🤖 | **AI/ML acceleration** | Neural networks for thermal-feedback modeling, interpolation and flux reconstruction on top of fission-matrix databases. |
| 🌙 | **Advanced reactors & space** | Heat-pipe microreactors, molten-salt reactors, research-reactor safety bases and lunar fission surface power. |

> 🧭 **Status note.** The method foundations (fission matrix, tRAPID kinetics, FM-CRd control rods) are published and experimentally validated. The OpenMC implementations, AI/ML acceleration and advanced-reactor applications below are **active development**, not finished results.

---

## 🧩 How the pieces fit

```mermaid
flowchart LR
    A["⚛️ OpenMC<br/>reactor model"] --> B["🎲 Fixed-source tallies<br/>FM / TFM coefficients"]
    B --> C[("🗄️ HDF5 database<br/>tfmines")]
    C --> D["⚡ Fast solvers<br/>k-eff · flux · kinetics"]
    D --> E["🛰️ UQ · optimization<br/>digital twins"]
    classDef n fill:#002554,stroke:#00b4d8,color:#fff,stroke-width:2px;
    class A,B,C,D,E n;
```

---

## 📦 Featured software

| Project | What it does | Status |
|---|---|---|
| 📚 [**CSM Open-Source Reactor Model Library**](https://github.com/M-PRISM-Colorado-School-of-Mines/CSM-Open-source-Reactor-Model-Library) | Independent, documented OpenMC models. First release: the **IAEA TECDOC-643** generic 10 MW LEU research reactor. Heat-pipe microreactor, lunar FSP, MSRE, pebble-bed HTGR and Radiant Kaleidos directories are reserved for upcoming models. | ![public](https://img.shields.io/badge/public-2ea44f?style=flat-square) ![MIT](https://img.shields.io/badge/MIT-blue?style=flat-square) |
| 🧮 **tfmines** | Transient Fission Matrix solver with OpenMC integration: extracts FM tallies from statepoints, solves for k-eff, fission source and importance, propagates coefficient uncertainties, and runs time-dependent kinetics (FM-CRd control rods, β<sub>eff</sub>, Λ, Rossi-α). Python by default, optional OpenMP C++ engine. | ![in development](https://img.shields.io/badge/in_development-f4a261?style=flat-square) |
| 🖥️ **slurm-manager** | Small Python library to prepare and submit Slurm jobs on a single-node workstation, built for the group's own compute. | ![in development](https://img.shields.io/badge/in_development-f4a261?style=flat-square) |

Other work in the lab includes OpenMC models of university research reactors (verified code-to-code against MCNP), TRIGA safety-basis modeling, and autonomy for lunar power systems.

---

## 📖 Selected publications from the method lineage

- **tRAPID**: *A Novel Hybrid Deterministic and Monte Carlo Neutron Transport Formulation and Algorithm for Accurate and Fast 3-D Reactor Kinetics*, Mascolino & Haghighat, **Nuclear Science and Engineering** 198 (2024)
- **Experimental validation of 3-D kinetics** on the JSI TRIGA Mark-II, Mascolino, Pungerčič, Snoj & Haghighat, **Progress in Nuclear Energy** 176 (2024)
- **FM-CRd**: *Development and Validation of New Algorithms for Control Rods Insertion Modeling in RAPID*, Mascolino, Haghighat & Snoj, **Annals of Nuclear Energy** 166 (2022)
- **Heat-pipe microreactors**: *The Fission Matrix Method for Criticality Search in Heat-Pipe Micro Reactors*, Vita et al., **Annals of Nuclear Energy** (2027)
- 📝 **Uncertainty quantification** *(preprint, under review)*: *Uncertainty Quantification for the Fission Matrix Method: A Rigorous Mathematical Framework and Computationally Efficient Alternatives*, Mascolino, submitted to **Nuclear Science and Engineering** · [arXiv:2609.33161](https://arxiv.org/abs/2609.33161)

---

## 🤝 Partners

<div align="center">

| 🇸🇮 **Jožef Stefan Institute** | 🇮🇹 **Politecnico di Milano** | 🎓 **Virginia Tech** |
|:---:|:---:|:---:|
| TRIGA Mark-II experiments and validation → [JSI-Mines-Collaboration](https://github.com/JSI-Mines-Collaboration) | Fuel performance, fusion and multi-physics → [PoliMI-Mines-Collaboration](https://github.com/PoliMI-Mines-Collaboration) | Origin of the RAPID code system and the fission-matrix lineage |
| 🇮🇹 **Politecnico di Torino** | 🏛️ **University of Missouri** | |
| Fission-matrix methods for heat-pipe microreactors | Research-reactor modeling (MURR) | |

</div>

---

## 🚀 Get involved

- 🧑‍🎓 **Students**: we work with PhD, MS and undergraduate researchers across nuclear engineering and computational physics.
- 🔧 **Contributors**: open an issue or pull request on any public repository.
- 📬 **Collaborators**: reach out through [vmascolino.com](https://www.vmascolino.com).

<div align="center">

<img src="https://raw.githubusercontent.com/M-PRISM-Colorado-School-of-Mines/.github/main/profile/footer.svg" alt="M-PRISM, Colorado School of Mines" width="100%"/>

</div>
