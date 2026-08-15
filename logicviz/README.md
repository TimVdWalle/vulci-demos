<!-- Phase: Phase 15B demo -->

# LogicViz

LogicViz is a terminal-based Boolean logic-circuit visualizer written entirely
in Vulci. It evaluates three circuits and draws their inputs, gates, intermediate
signals, and final outputs.

## Vulci phase

LogicViz is a **Phase 15** demo, built and verified with the Phase 15B Vulci
interpreter (`v0.15.0`). It uses Phase 15 file imports to split the program into
its model, circuit data, and entry-point renderer.

The program also demonstrates structs, methods, nullable recursive fields,
enums, tuples, string interpolation, type inspection, and Boolean expressions.

## Files

| ID | File | Responsibility |
| --- | --- | --- |
| `logicviz-file-main` | [`main.vci`](main.vci) | Validates each display schema and renders the terminal interface. |
| `logicviz-file-model` | [`model.vci`](model.vci) | Defines gate types, circuit nodes, validation, and evaluation. |
| `logicviz-file-circuit` | [`circuit.vci`](circuit.vci) | Constructs the three demonstration circuits and their input values. |

## Included circuits

| ID | Expression |
| --- | --- |
| `logicviz-circuit-simple` | `AND(A, B)` |
| `logicviz-circuit-medium` | `OR(AND(A, B), C)` |
| `logicviz-circuit-advanced` | `OR(AND(A, NOT(B)), XOR(C, D))` |

## Run

From the `vulci-demos` repository root:

```shell
vulci logicviz/main.vci
```

Or from this directory:

```shell
vulci main.vci
```

Green signals are `true`; red signals are `false`. Each circuit has a boxed
header containing its final output, followed by its circuit diagram.
