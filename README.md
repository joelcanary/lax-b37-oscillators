# Two oscillators of the rule B37/S2378 that Conway's rule does not sustain

**Lax Lean Archive record [`lax-834858`](https://laxarchive.org/lax-834858/)** — registered, permanent and citable.
Every statement in `concepts/` is proved in `proofs/` with no assumptions: **4 of 4 statements proved**,
rebuilt by the archive on its own machines against a pinned Mathlib before registration.

The outer-totalistic rule $B37/S2378$ — a dead cell is born with 3 or 7 live neighbours, a live cell survives with 2, 3, 7 or 8 — was selected by exhaustive search and runs as the background automaton of a public website. An exhaustive census of the 51,472 seeds whose bounding box is exactly $4 \times 4$, classified by recurrence up to translation, produced 96 distinct objects (phases of an oscillator counted together) with oscillator periods 2, 3, 10 and 32; the same census under Conway's $B3/S23$ produced 81 objects with periods 2 and 3 only. This submission archives the two objects that separate the rules. The period-10 oscillator has 11 live cells in its smallest phase and the period-32 one has 13 in the phase shown; each is given as an explicit board whose margin is wide enough that no phase of the cycle reaches the border, so the statements are statements about the patterns on the plane. Four statements are proved: the two periods, the minimality of the first, and the failure of Conway's rule to return the first pattern to itself within those ten generations. Every proof is a finite evaluation closed by `decide` in the kernel, with no `native_decide` and no assumption beyond `propext`.

## What is inside

| Concept | Type | Title | Proved / stated |
|---|---|---|---|
| `Oscillators` | theorem | Two oscillators of the rule B37/S2378 that Conway's rule does not sustain | 4 / 4 |

Each concept file states its results as `axiom`s beside a natural-language description
(that is the archive's format: statements are separated from proofs); the proof of each
one lives in `proofs/` and is checked by the Lean kernel. `build-output.json` is the
archive's own build record for this source commit.

## How to cite

In LaTeX, cite the record id: `\cite{lax-834858}`. The archive resolves it to the exact
statements and proofs, and a registered record cannot change under the citation
(a correction would be a new record that supersedes this one).

```bibtex
@misc{lax834858,
  author = {Cruz Cabrera, Joel},
  title = {Two oscillators of the rule B37/S2378 that Conway's rule does not sustain},
  year = {2026},
  howpublished = {Lax Lean Archive, record lax-834858},
  url = {https://laxarchive.org/lax-834858/}
}
```

Author: Joel Cruz Cabrera, ORCID [0009-0005-4048-1237](https://orcid.org/0009-0005-4048-1237).

## Rebuilding it

```bash
npm install -g lax-archive
lax build          # Lean v4.33.0, Mathlib db584cd6d46c
```

The pins are in `manifest.yaml`; the archive's build of this commit
(`f37a1f3`) is recorded in `build-output.json`
(`archiveSha` `1180c8452aa4`).

## Related

- The five records and their live counts: https://kodamaseclabs.com/publications
- The note on the rule, with the exhaustive census: doi:10.5281/zenodo.22974274 (all versions).
- Code, data and the note's sources: https://github.com/joelcanary/life-like-rule-b37s2378

## Use of AI

An AI tool (an agent running on the author's machine) wrote the Lean under the
author's direction; the author set the statements, reviewed every declaration
and checked the build before submitting. The archive then rebuilt everything
independently. What is proved is exactly what the kernel accepted, no more.

## License

Apache-2.0 (the archive's required license), see `LICENSE`.

<details><summary>BibTeX entries the record itself cites</summary>

```bibtex
@book{gardner1983,
  author = {Gardner, Martin},
  title = {Wheels, Life and Other Mathematical Amusements},
  publisher = {W. H. Freeman},
  year = {1983}
}
```
</details>
