# Bcap (or Binary 🧢)
A data format in binary (better than BSON)

## Specification

### Data types
 - `bool` - `0x01`
 - `int` - `0x02`
 - `float` - `0x03`
 - `string` - `0x04`

### Definitions
 - `null` - `0x00`
 - `false` - `0x01`
 - `true` - `0x02`

### Example
```
\0x01\0x01
|    |   |
  ^    ^
  |    └- Value (true)
Defining a bool

\0x02\0x0F
|    |   |
  ^    ^
  |    └- Value (15)
Defining an int

\0x04bom dia\0x00
|    |          |
  ^        ^
  |        └- Value ("bom dia") and EOS (end of string)
Defining a string
```