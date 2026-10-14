# Students — MICROSCOPY

**Project:** MICROSCOPY  
**Category:** SCIENTIFIC_LAB  
**Upstream:** https://github.com/IBM/MicroscoPy  
**Pinned commit:** `afc20d1d74053fe1d923274ad4d8b0caf470d1ef`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `bca2025104ab16f8a10d886fb613269040957d0c1b838537bab6a947003e0eb9`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `afc20d1d74053fe1d923274ad4d8b0caf470d1ef`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `bca2025104ab16f8a10d886fb613269040957d0c1b838537bab6a947003e0eb9`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
