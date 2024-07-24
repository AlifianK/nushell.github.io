---
title: polars is-unique
categories: |
  dataframe
version: 0.95.0
dataframe: |
  Creates mask indicating unique values.
usage: |
  Creates mask indicating unique values.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# `polars is-unique` for [dataframe](/commands/categories/dataframe.md)

<div class='command-title'>Creates mask indicating unique values.</div>

## Signature

```> polars is-unique {flags} ```


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Create mask indicating unique values
```nu
> [5 6 6 6 8 8 8] | polars into-df | polars is-unique
╭───┬───────────╮
│ # │ is_unique │
├───┼───────────┤
│ 0 │ true      │
│ 1 │ false     │
│ 2 │ false     │
│ 3 │ false     │
│ 4 │ false     │
│ 5 │ false     │
│ 6 │ false     │
╰───┴───────────╯

```

Create mask indicating duplicated rows in a dataframe
```nu
> [[a, b]; [1 2] [1 2] [3 3] [3 3] [1 1]] | polars into-df | polars is-unique
╭───┬───────────╮
│ # │ is_unique │
├───┼───────────┤
│ 0 │ false     │
│ 1 │ false     │
│ 2 │ false     │
│ 3 │ false     │
│ 4 │ true      │
╰───┴───────────╯

```