# Educators — MICROSCOPY

**Project:** MICROSCOPY  
**Category:** SCIENTIFIC_LAB  
**Upstream:** https://github.com/IBM/MicroscoPy  
**Pinned commit:** `afc20d1d74053fe1d923274ad4d8b0caf470d1ef`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `bca2025104ab16f8a10d886fb613269040957d0c1b838537bab6a947003e0eb9`  
**Date:** October 2026

## Teaching with MICROSCOPY

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `bca2025104ab16f8a10d886fb613269040957d0c1b838537bab6a947003e0eb9` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
