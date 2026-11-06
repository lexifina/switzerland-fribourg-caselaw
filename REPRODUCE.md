# Reproducing this repository

Input: the Parquet files listed below, revision `fecc2c971945cacd914c63b54ee22db9149e58c9` of the `voilaj/swiss-caselaw` dataset
(`https://huggingface.co/datasets/voilaj/swiss-caselaw/resolve/fecc2c971945cacd914c63b54ee22db9149e58c9/<file>`), plus `graph/statute_references.parquet`
from the same revision, and lexifina/switzerland-law `main` for the overlay's `law_commit`.

```
python tools/build.py fr <cache with data/ and graph/> <empty folder> --today 2026-11-06
```

Needs Python 3 and `duckdb`. Gives 14,853 decision commits and one documentation commit, hash for hash.

## SHA-256 of the input files

```
47bc536264e072a224b318807802cfcecb8bde3d2468144ddc1c7dc72b2ecb32 *fr_anwaltsaufsicht.parquet
0890f465df15996c693d6f4293699297029ee01533819ecdd29ce9b46736bcc2 *fr_gerichte.parquet
```
