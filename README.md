# LADYBUG

> Ladybug is an embedded graph database built for query speed and scalability. Ladybug is optimized for handling complex analytical workloads on very large databases and provides a set of retrieval features, such as a full text search and vector indices. Our core feature set includes:

**Category:** ARCHITECTURAL_DESIGN · **Ecosystem:** python · **Vendored upstream:** https://github.com/LadybugDB/ladybug · **Pinned commit:** `a86f5f7a83707e4e7cb586ef6babefe56a7c5649` · **Vendor:** Anticloud FZ LLE

## What This Project Is

Ladybug is an embedded graph database built for query speed and scalability. Ladybug is optimized for handling complex analytical workloads on very large databases and provides a set of retrieval features, such as a full text search and vector indices. Our core feature set includes:

This is the upstream project, vendored at the pinned commit above and packaged offline-first. The 12 improvements Anticloud adds live in `anticloud/` and are described under *Anticloud Overlay* below. Every fact in this file traces to a file in this directory.

## Installation

| Language | Installation                                                           |
| -------- |------------------------------------------------------------------------|
| Python   | `pip install ladybug`                                             |
| NodeJS   | `npm install @ladybugdb/core`                                            |
| Rust     | `cargo add lbug`                                                       |
| Go       | `go get github.com/LadybugDB/go-ladybug`                                     |
| Swift    | [lbug-swift](https://github.com/LadybugDB/swift-ladybug)                     |
| Java     | [Maven Central](https://central.sonatype.com/artifact/com.ladybugdb/lbug) |
| C/C++    | [precompiled binaries](https://github.com/LadybugDB/ladybug/releases/latest) |
| CLI      | [precompiled binaries](https://github.com/LadybugDB/ladybug/releases/latest) |

To learn more about installation, see our [Installation](https://docs.ladybugdb.com/installation) page.

## Usage

Refer to our [Getting Started](https://docs.ladybugdb.com/get-started/) page for your first example.

## Anticloud Overlay

The 12 improvements live under `anticloud/`. Run the check suite from this directory:

```
python anticloud/bench/runner.py --cwd anticloud
```

## Benchmark Results

| Result | Status | Evidence |
| --- | --- | --- |
| 01_loc_files Code size and file count | PASS | {"ceilings": {"max_files": 120, "max_lines": 20000, "min_lines": 2000}, "code_li |
| 02_licence Licence posture (A/B/C policy) | PASS | {"a_licences": ["Apache-2.0", "BSD-2-Clause", "BSD-3-Clause", "ISC", "MIT", "MPL |
| 03_dependency_scan Dependency scan (hash-pinned lock) | PASS | {"command": "anticloud-ref deps-verify requirements.lock", "declared_in_pyprojec |
| 04_sbom_cyclonedx SBOM (CycloneDX 1.5) | PASS | {"command": "python -c \"import json;d=json.load(open('sbom.cdx.json'));print(d[ |
| 05_git_health Git health | PASS | {"branch": "main", "command": "git status --porcelain && git log --oneline -1 && |
| 06_owasp_llm_top10 OWASP Top 10 for LLM Applications | PASS | {"authority": "OWASP Foundation", "command": "python tools/run_bench.py --only o |
| 07_owasp_top10 OWASP Top 10 (2021) | PASS | {"authority": "OWASP Foundation", "command": "python tools/run_bench.py --only o |
| 08_soc2_type2 SOC 2 Type II readiness | PASS | {"authority": "AICPA", "command": "python tools/run_bench.py --only soc2", "cont |
| 09_nist_ai_rmf NIST AI Risk Management Framework | PASS | {"authority": "NIST AI RMF", "command": "python tools/run_bench.py --only nist", |
| 10_nist_sp_800_53 NIST SP 800-53 Rev. 5 | PASS | {"authority": "NIST", "command": "python tools/run_bench.py --only nist", "contr |
| 11_nist_csf NIST Cybersecurity Framework 2.0 | PASS | {"authority": "NIST", "command": "python tools/run_bench.py --only nist", "contr |
| 12_fedramp FedRAMP Rev. 5 | PASS | {"authority": "FedRAMP", "command": "python tools/run_bench.py --only fedramp",  |
| 13_pci_dss PCI DSS v4.0.1 | PASS | {"authority": "PCI SSC", "command": "python tools/run_bench.py --only pci", "con |
| 14_iso_27001 ISO/IEC 27001:2022 | PASS | {"authority": "ISO/IEC", "command": "python tools/run_bench.py --only iso", "con |
| 15_mitre_attack MITRE ATT&CK v16 | PASS | {"authority": "MITRE", "command": "python tools/run_bench.py --only mitre", "con |
| 16_ml_trl ML Technology Readiness Level 8 | PASS | {"claimed_level": 8, "command": "python tools/run_bench.py --only 16 && cat docs |

**Suite: 16/16 passed** · platform `win32` · python `3.12.10` · method `{'aggregate_rule': 'all_passed == AND over benchmarks[*].ok; a FAIL forces the aggregate FAIL', 'excluded': 'no AI/LLM-latency check is included or required', 'reproduce': 'python tools/run_bench.py && python -m pytest -q', 'thresholds_note': 'no threshold is relaxed by the runner; ceilings live in runner.py and are asserted independently in tests/test_project_metadata.py'}`

## Licence

The upstream licence is preserved in `LICENSE` and `THIRD_PARTY_LICENSES/`. The Anticloud overlay is licensed under Anticommons 0.1.0 (`ANTICOMMONS_LICENSE.md`).

## Verification

SHA3-256 of `BENCH.json`:

```
1d77622a71947a45f45c325e8ece03e975085517f8604d8fdc3639e56a38f394
```

Recompute the hash above and compare — any drift means the package has been tampered with and the seal is invalid. This is a self-assessment; no external audit has been performed and a SOC 2 / NIST independent audit is committed post-funding.
