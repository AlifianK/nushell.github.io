---
title: polars dummies
categories: |
  dataframe
version: 0.95.0
dataframe: |
  Creates a new dataframe with dummy variables.
usage: |
  Creates a new dataframe with dummy variables.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# `polars dummies` for [dataframe](/commands/categories/dataframe.md)

<div class='command-title'>Creates a new dataframe with dummy variables.</div>

## Signature

```> polars dummies {flags} ```

## Flags

 -  `--drop-first, -d`: Drop first row


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Create new dataframe with dummy variables from a dataframe
```nu
> [[a b]; [1 2] [3 4]] | polars into-df | polars dummies
╭───┬─────┬─────┬─────┬─────╮
│ # │ a_1 │ a_3 │ b_2 │ b_4 │
├───┼─────┼─────┼─────┼─────┤
│ 0 │   1 │   0 │   1 │   0 │
│ 1 │   0 │   1 │   0 │   1 │
╰───┴─────┴─────┴─────┴─────╯

```

Create new dataframe with dummy variables from a series
```nu
> [1 2 2 3 3] | polars into-df | polars dummies
╭───┬─────┬─────┬─────╮
│ # │ 0_1 │ 0_2 │ 0_3 │
├───┼─────┼─────┼─────┤
│ 0 │   1 │   0 │   0 │
│ 1 │   0 │   1 │   0 │
│ 2 │   0 │   1 │   0 │
│ 3 │   0 │   0 │   1 │
│ 4 │   0 │   0 │   1 │
╰───┴─────┴─────┴─────╯

```