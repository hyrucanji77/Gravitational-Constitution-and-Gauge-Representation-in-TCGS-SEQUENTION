# Reproducibility

## Version identity

The manuscript is version 5 (45 pages, 39 numbered references); the computation is release 4. The five scientific programs and dependency pins reproduce the exact bytes cited by manuscript reference [37], commit `950f4a59f7b9f0dd8425ffb4fa37e429c3c0b4a5` in `hyrucanji77/TCGS-SEQUENTION-protocol/papers/gravitational_constitution`.

The original archive remains available. No changes to the mathematical code or manuscript are required to use this dedicated repository. `provenance/MANUSCRIPT.json` identifies the separately distributed PDF by size, SHA-256, and legacy MD5; it does not claim that the PDF is stored in this repository.

## Environment and execution

The reference environment is Python 3.13.5 with mpmath 1.3.0, SymPy 1.14.0, NumPy 2.3.5, and SciPy 1.17.0. Install the dependencies in an isolated environment, then run from the repository root:

```sh
python -m pip install -r code/requirements.txt
python code/verify_results.py --output results/results.json
python code/verify_extensions.py --output results/extension_results.json
python code/verify_nonlinear_slab.py --output results/nonlinear_slab_results.json
python code/verify_model_discrimination.py --output results/model_discrimination_results.json
python code/verify_empirical_reach.py --output results/empirical_reach_results.json
```

The default output of each program, when `--output` is omitted, is beside that program. All five return a nonzero exit status on a failed required check. They require no network access after dependencies are installed.

Expected check counts are 30, 53, 23, 70, and 100 respectively: **276 in total**. `verification_summary.json` records the dedicated repository's execution; `provenance/release4_verification_summary.json` preserves the source release's record. `results/` holds complete reports and the tolerance thresholds.

## Integrity

The checksum list covers the five programs and pinned dependency file. On systems with `sha256sum`:

```sh
(cd code && sha256sum -c SHA256SUMS.txt)
```

The hashes match the source snapshot. Optimizer iteration counts and final floating-point values may vary slightly between platforms; the stated program tolerances, stationarity tests, resolution comparisons, and convergence checks govern reproducibility rather than identical JSON bytes.

## Scope of the checks

These reports contain model calculations and transcribed published inputs, not new experimental observations. They do not certify a stellar two-body remainder, an accessible observing interval, a complete spectral-tower exclusion likelihood, a relativistic or ultraviolet completion, or an independent recomputation of the Partanen–Tulkki loop integrals. `docs/SOURCE_PROVENANCE.md`, `docs/EMPIRICAL_REACH.md`, and `REFERENCES.md` identify the primary sources and limitations.

The conditional quadratic interval can open above the stated tolerance thresholds while remaining insufficient for an admissible observation. Newton belongs to the matched-gradient null class. The real-space statistic must not be replaced by purely axial Fourier ratios.

## Distribution

LaTeX sources, bibliography source files, compilation products, internal framework compilations, and source-containing archives are excluded. The manuscript PDF and nine individual supporting-reference PDFs are provided separately in the source-free publication bundle. Third-party access routes appear in `REFERENCES.md`; their licenses and version identities remain source-specific.
