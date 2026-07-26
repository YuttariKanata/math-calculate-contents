# Recursive Curve Construction

This repository generates the recursive patterns `A_n` and `B_n`.

## Initial patterns

The construction starts from two unit-square patterns, `A₀` and `B₀`.

Each pattern consists of four disjoint line segments connecting designated points on the boundary of the unit square.

The boundary points are

- Left: `(0,1/3)`, `(0,2/3)`
- Right: `(1,1/3)`, `(1,2/3)`
- Bottom: `(1/3,0)`, `(2/3,0)`
- Top: `(1/3,1)`, `(2/3,1)`

The connections are

### A₀

- `(1/3,0)` ↔ `(1/3,1)`
- `(2/3,0)` ↔ `(1,1/3)`
- `(0,1/3)` ↔ `(1,2/3)`
- `(0,2/3)` ↔ `(2/3,1)`

### B₀

- `(1/3,0)` ↔ `(0,1/3)`
- `(2/3,0)` ↔ `(1/3,1)`
- `(0,2/3)` ↔ `(1,2/3)`
- `(2/3,1)` ↔ `(1,1/3)`

## Recursive construction

For every `n ≥ 0`, larger patterns are obtained by arranging four copies of the previous patterns in a 2×2 grid.

```text
A_{n+1}

+-----+-----+
| A_n | B_n |
+-----+-----+
| B_n | A_n |
+-----+-----+
```

```text
B_{n+1}

+-----+-----+
| B_n | A_n |
+-----+-----+
| A_n | B_n |
+-----+-----+
```

Whenever two neighboring tiles share a boundary, the corresponding boundary points are identified so that the curves connect continuously across tile boundaries.

## Visualization

Each generated pattern occupies a square.

The background is white and every curve is drawn in black.

The program can generate an image for arbitrary `A_n` or `B_n`.

## Cycle detection

The generated curves are internally represented as a graph.

Vertices correspond to connection points, and edges correspond to curve segments.

Cycle detection is performed using graph traversal (DFS), allowing the program to determine whether `A_n` or `B_n` contains a closed loop.

## Large output images

The generated images for `A₉` and `B₉` are too large to be included in this GitHub repository because of GitHub's file size limits.

They are available on Google Drive instead:

- **A₉:** [A9 (Google Drive)](https://drive.google.com/file/d/1oIu-trwmm56rFLJ6CMdE5XsxNsLCguG2/view?usp=sharing)
- **B₉:** [B9 (Google Drive)](https://drive.google.com/file/d/1ldMG0ZWsKmrtR83zuncmWNr118iBIAcI/view?usp=sharing)
