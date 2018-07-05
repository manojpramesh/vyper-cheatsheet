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

Signed : `int128`

#### Operators 

*Comparison*: `<, >, <=, >=, ==, !=`
*Arithmetic*: `+, -, unary -, *, /, **, %, min(), max()`
*Bitwise*: `bitwise_and(), bitwise_not(), bitwise_or(), bitwise_xor(), shift()`

> In `shift(a, _shift)` _shift must be of the type int128, where positive _shift means a left shift and negative _shift means a right shift.


### Decimels

`decimal`: Holds a decimal fixed point value.

#### Operators 

*Comparison*: `<, >, <=, >=, ==, !=`
*Arithmetic*: `+, -, unary -, *, /, **, %`


### Address

`address`: Holds an Ethereum address (20 byte value).

#### Members

`balance`: Get balance of the address in `wei_value`.
`codesize`: Get code stored at this address. Returns `int128`.


### Time

`timestamp`: Holds the time
`timedelta`: Time difference

> Two `timedelta` or a `timedelta` and a `timestamp` can be added together . It is not possible to add two `timestamp` values.

### wei_value

`wei_value`: Holds amount of Ether in its smallest denomination.

### Boolean

`bool`: true or false

**Operators**: not, and, or, ==, !=


### Structs

User defined data type.

```
<struct_name>: {
    <value>: <data_type>,
    <value>: <data_type>,
    ...
}
```

### Mappings

Mappings are similar to hash tables.

```
<mapping_name>: <value_type>[<key_type>]
```

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
