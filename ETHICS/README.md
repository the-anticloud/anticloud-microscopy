# Ethics — MICROSCOPY

**Project:** MICROSCOPY  
**Category:** SCIENTIFIC_LAB  
**Upstream:** https://github.com/IBM/MicroscoPy  
**Pinned commit:** `afc20d1d74053fe1d923274ad4d8b0caf470d1ef`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `bca2025104ab16f8a10d886fb613269040957d0c1b838537bab6a947003e0eb9`  
**Date:** October 2026

## Position

MICROSCOPY is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
