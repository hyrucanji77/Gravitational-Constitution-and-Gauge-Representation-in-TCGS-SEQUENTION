# Gravitational Constitution and Gauge Representation in TCGS–SEQUENTION

## Constitutive Response, Geometric Completion, and Quantum Counterterms

**Henry Arellano-Peña · Manuscript version 5 · Computational release 4 · 1 November 2026**

This repository provides the computational supplement for the 45-page manuscript, with its five verification programs, numerical reports, source provenance, dependency pins, and complete 39-entry reference index. The manuscript separates gauge representation, constitutive response, geometric completion, and source interpretation.

The five programs preserve the exact bytes of the [release-4 snapshot cited in reference 37](https://github.com/hyrucanji77/TCGS-SEQUENTION-protocol/tree/950f4a59f7b9f0dd8425ffb4fa37e429c3c0b4a5/papers/gravitational_constitution). That immutable citation remains valid; this dedicated repository provides a separate distribution of the same calculations.

### Scientific scope

The calculations cover reflecting and Dirichlet slab responses, the compactification identity, the local constitutive null sector, nonlinear thin-slab reduction, a constant-background tangent kernel, a specified real-space AQUAL–QUMOND discriminator, and conditional observing-window and uncertainty calculations. Newton belongs to the matched-gradient null class. Purely axial Fourier responses are not the real-space axis-force statistic. The nonlinear reduction requires a smooth uniformly elliptic branch, and the stellar two-body approximation is not certified by the local Taylor or parity calculations.

The laboratory-compatible slab is effectively AQUAL on the smooth astrophysical scales considered. The historical Yukawa comparison is a single-mode benchmark, not a complete-tower likelihood bound. The unit-coefficient identification a_* = c^2/L is excluded for the stated universal unscreened realization. A conditional observing interval can open under relaxed budgets without establishing an admissible experiment.

### Reproduce

```sh
python -m pip install -r code/requirements.txt
python code/verify_results.py
python code/verify_extensions.py
python code/verify_nonlinear_slab.py
python code/verify_model_discrimination.py
python code/verify_empirical_reach.py
```

| Program | Checks |
|---|---:|
| `code/verify_results.py` | 30 |
| `code/verify_extensions.py` | 53 |
| `code/verify_nonlinear_slab.py` | 23 |
| `code/verify_model_discrimination.py` | 70 |
| `code/verify_empirical_reach.py` | 100 |
| **Total** | **276** |

Each program accepts `--output PATH`, writes its default report beside the script, and returns a nonzero exit status on a failed required check. No network access is required after dependency installation. These are finite symbolic and numerical consistency checks, not empirical observations, a proof of every analytical hypothesis, a catalogue fit, a full-tower likelihood analysis, or an independent quantum-loop calculation.

### Versions and citation

Manuscript version 5 and computational release 4 are different version identifiers. The original full computational snapshot is `950f4a59f7b9f0dd8425ffb4fa37e429c3c0b4a5`, in `hyrucanji77/TCGS-SEQUENTION-protocol`, directory `papers/gravitational_constitution`. No journal acceptance or manuscript DOI is asserted.

### License

The original article, code, and documentation are licensed under Creative Commons Attribution 4.0 International (CC BY 4.0). Cited third-party works retain their respective rights. LaTeX sources, compilation files, source-containing archives, and internal framework compilations are not distributed here.
