---
title: polars cumulative
categories: |
  dataframe
version: 0.95.0
dataframe: |
  Cumulative calculation for a series.
usage: |
  Cumulative calculation for a series.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# `polars cumulative` for [dataframe](/commands/categories/dataframe.md)

<div class='command-title'>Cumulative calculation for a series.</div>

## Signature

```> polars cumulative {flags} (type)```

## Flags

 -  `--reverse, -r`: Reverse cumulative calculation

## Parameters

 -  `type`: rolling operation


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Cumulative sum for a series
```nu
> [1 2 3 4 5] | polars into-df | polars cumulative sum
╭───┬──────────────────╮
│ # │ 0_cumulative_sum │
├───┼──────────────────┤
│ 0 │                1 │
│ 1 │                3 │
│ 2 │                6 │
│ 3 │               10 │
│ 4 │               15 │
╰───┴──────────────────╯

```