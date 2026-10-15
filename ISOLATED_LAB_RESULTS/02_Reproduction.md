# Reproduction — ARCHITECTURAL_DESIGN/LADYBUG

```bat
cd /d E:\fenta\Downloads\The Anticloud\ANTICLOUD_REPOS\ARCHITECTURAL_DESIGN\LADYBUG
python tools\run_bench.py --out BENCH.json --quiet
python -c "import json;d=json.load(open('BENCH.json'));print(d['all_passed'],d['passed'],'/',d['total'])"
```

Last run aggregate: 16/16 (PASS); evidence SHA3-256 `bf4d630089aefe3dcfce368016032c8e133b0f01c1ba731049917016013b5a99`.
