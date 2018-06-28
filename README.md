# vyper-cheatsheet

### Motivation
This document is a cheatsheet for Vyper that you can use to write Smart Contracts for Ethereum.

This guide is not intended to teach you Vyper from the ground up, but to help developers with basic knowledge who may struggle to get familiar with Smart Contracts and Blockchain because of the Vyper concepts used.

> Note: Vyper is very similar to Python and if you have basic knowledge in Python, it's easier to learn Vyper.

## Table of contents

[WIP]

## Types

### Integer

Unsigned : `uint256`

Signed : `int128` | `int256`

### Address

`address`: Holds an Ethereum address (20 byte value).

### Timestamp

`timestamp`: Holds the time

### Time delta

`timedelta`: Time difference

### wei_value

`wei_value`: Holds amount of Ether in its smallest denomination.

### Boolean

`bool` : true or false


## Functions

### Structure

```
def <function_name>(<param_name>: <param_type>, ...) -> <return_type>:
    <definition>
    ...
```

### Constructor

Function which is called during contract creation

```python
def __init__(_a: address, _b: bool):
  self.a = _a;
  self.b = _b
```

