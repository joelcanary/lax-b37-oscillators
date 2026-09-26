# Two oscillators of the rule B37/S2378 that Conway's rule does not sustain

Lean 4 statements and kernel-checked proofs, prepared for the
[Lax Lean Archive](https://laxarchive.org/). Every statement in `concepts/` is proved
in `proofs/`: **4 of 4 statements proved, no assumptions** beyond `propext`.

The outer-totalistic rule $B37/S2378$ — a dead cell is born with 3 or 7 live neighbours, a live cell survives with 2, 3, 7 or 8 — was selected by exhaustive search and runs as the background automaton of a public website. An exhaustive census of the 51,472 seeds whose bounding box is exactly $4 \times 4$, classified by recurrence up to translation, produced 96 distinct objects (phases of an oscillator counted together) with oscillator periods 2, 3, 10 and 32; the same census under Conway's $B3/S23$ produced 81 objects with periods 2 and 3 only. This submission archives the two objects that separate the rules. The period-10 oscillator has 11 live cells in its smallest phase and the period-32 one has 13 in the phase shown; each is given as an explicit board whose margin is wide enough that no phase of the cycle reaches the border, so the statements are statements about the patterns on the plane. Four statements are proved: the two periods, the minimality of the first, and the failure of Conway's rule to return the first pattern to itself within those ten generations. Every proof is a finite evaluation closed by `decide` in the kernel, with no `native_decide` and no assumption beyond `propext`.

## What is inside

| Concept | Type | Statements | Proved |
|---|---|---|---|
| `LaxOsc.Oscillators` | theorem | 4 | 4 |

* `p10_period` — `houseStep^[10] p10 = p10`
* `p10_period_minimal` — no `k < 10` returns the pattern to itself
* `p32_period` — `houseStep^[32] p32 = p32`
* `p10_not_conway` — under `B3/S23` the same pattern does not return within ten generations

## How the boards were found

`research/vida/censo_b37.py` in the author's project evolves every non-empty seed of a
`4 x 4` box alone on the plane and classifies the result by recurrence up to
translation. The two boards here are the two oscillators of that census whose periods
do not occur in the same census under `B3/S23`. The margins (4 and 7 empty cells) are
the smallest for which no phase of the cycle touches the border.

## Licence

Apache-2.0.
