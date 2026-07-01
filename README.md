# LILR Atlas

Interactive browser for haplotype-resolved copy-number, sequence, and
structural genotyping of the eleven human *LILR* genes (chr19q13.4) across
232 HPRC individuals (464 phased assemblies).

## View the atlas

Once GitHub Pages is enabled for this repository, the atlas is served at
the repo's Pages URL - opening that URL loads [`index.html`](index.html)
directly.

If you don't have Pages access, you can also clone this repo and open
`index.html` in any browser locally:

```bash
git clone <repo-url> lilr-atlas
xdg-open lilr-atlas/index.html   # or: open / start
```

## What's in here

| File | Description |
|---|---|
| `index.html` | The atlas - single self-contained file. Bundles 3Dmol.js, Plotly.js, allele FASTAs/JSONs, and AlphaFold PDB structures. ~19 MB. |
| `.nojekyll` | Disables GitHub Pages' Jekyll processing so the bundled assets are served byte-for-byte. |
| `README.md` | This file. |

## Atlas tabs

1. **Overview** - per-sample lookup across all 11 LILRs
2. **Sequence Diversity** - per-locus distinct-allele counts (HPRC + EURA/AA short-read)
3. **Copy Number** - per-superpop CN distributions, LILRA3 deletion, LILRA6 expansion
4. **Structural Haplotypes** - 14 distinct gene-order structures
5. **Linkage Disequilibrium** - Cramér's V per superpop
6. **Allele Registry** - provisional content-addressable allele names
7. **Disease Associations** - GWAS Catalog hits and per-allele rsID carrier calls

## Source pipeline

The atlas is built from the
[`lilr_pangenome`](../lilr_pangenome) pipeline output (not in this repo).
To regenerate it: `python analysis/build_atlas.py` from the source repo,
then copy the resulting `lilr_atlas.html` here as `index.html`.

## Citation

If you use the atlas, please cite the LILR pangenome manuscript (in
preparation). A `CITATION.cff` will be added once the manuscript is on
biorxiv/published.
