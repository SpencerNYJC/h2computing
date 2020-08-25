## Python Notes for H2 Computing

#### Operators
| Operator |    Function    |              Usage |
| -------- | :------------: | -----------------: |
| +        |    addition    |    ```1 + 1 = 2``` |
| -        |    subtract    |   ``` 2 - 1 = 1``` |
| /        |    division    |   ``` 2 / 2 = 1``` |
| *        |    multiply    |   ``` 2 * 2 = 4``` |
| **       |    exponent    |  ``` 3 ** 2 = 9``` |
| //       | floor-quotient | ``` 5 // 2 = 2 ``` |
| %        |     modulo     |    ```5 % 2 = 1``` |

#### Data types
1. Text Types
   *  ```str```
2. Numeric Types
   * ```int, float, complex```
3. Sequence Types
   * ```list, tuple, range```
4. Mapping Type
   * ```dict```
5. Set Types
   * ```set, frozenset```
6. Boolean Types
   * ```bool```
7. Binary Types
   * ```bytes, bytearray,memoryview```  

#### Commonly used types
```python
x = 5
#str, int, float, list, tuple, dict, set, bool
#to retrieve the data type of variable x
type(x)
```
```
Output: int
```

#### Comparators

| Usage    | Description                     | True examples      |
| -------- | ------------------------------- | ------------------ |
| `a == b` | a is equal to b                 | `1 == 1`           |
| `a != b` | a is not equal to b             | `1 != 2`           |
| `a > b`  | a is greater than b             | `2 > 1`            |
| `a >= b` | a is greater than or equal to b | `2 >= 1`, `1 >= 1` |
| `a < b`  | a is less than b                | `1 < 2`            |
| `a <= b` | a is less than or equal to b    | `1 <= 2`, `1 <= 1` |

| Usage     | Description                               | True example                      |
| --------- | ----------------------------------------- | --------------------------------- |
| `a and b` | a is True and b is True                   | `1 == 1 and 2 == 2`               |
| `a or b`  | a is True, b is True or they're both True | `False or 1 == 1`, `True or True` |

```python
>> a = 1
>> b = 2
>> a == b
False
>> a is not b
True
```

#### Booleans

```python
True
False
```

