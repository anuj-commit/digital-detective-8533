# Mission 5 - Numbers and data

## 1. Task / objective

Practise converting numbers between decimal, binary and hexadecimal, check the answers with Python, make a small converter, and learn how computers store text and data.

## 2. Work completed

### Task 5.1 - Number conversions by hand

| Question | Working and answer |
|---|---|
| Decimal 13 to binary | 13 = 8 + 4 + 1, so the 8, 4, 2, 1 places are 1, 1, 0, 1. Answer: `1101₂`. |
| Decimal 25 to binary | 25 = 16 + 8 + 1. The 16, 8, 4, 2, 1 places are 1, 1, 0, 0, 1. Answer: `11001₂`. |
| Binary 1010 to decimal | `1×8 + 0×4 + 1×2 + 0×1 = 10`. |
| Binary 1101 to decimal | `1×8 + 1×4 + 0×2 + 1×1 = 13`. |
| Hexadecimal A to decimal | A represents 10, so the answer is `10`. |
| Hexadecimal 1F to decimal | `1×16 + 15 = 31`, because F represents 15. |
| Binary 1111 to hexadecimal | `1111₂` is 15 in decimal, and 15 is F in hexadecimal. Answer: `F₁₆`. |

### Task 5.2 - Python verification

I used Python's built-in conversion functions in the interactive prompt. The answers matched my working.

| Expression | Result | Check |
|---|---|---|
| `bin(13)` | `'0b1101'` | Matches `1101₂`. |
| `bin(25)` | `'0b11001'` | Matches `11001₂`. |
| `int('1010', 2)` | `10` | Matches binary `1010`. |
| `int('1101', 2)` | `13` | Matches binary `1101`. |
| `hex(13)` | `'0xd'` | 13 is D in hexadecimal. |
| `hex(25)` | `'0x19'` | 25 is 19 in hexadecimal. |
| `int('A', 16)` | `10` | Matches hexadecimal A. |
| `int('1F', 16)` | `31` | Matches hexadecimal 1F. |
| `hex(int('1111', 2))` | `'0xf'` | Matches `F₁₆`. |

### Task 5.3 - Number converter

The program asks for a decimal integer and displays Python's binary and hexadecimal forms. I ran it with three positive numbers:

| Input | Binary output | Hexadecimal output |
|---:|---|---|
| 18 | `0b10010` | `0x12` |
| 42 | `0b101010` | `0x2a` |
| 255 | `0b11111111` | `0xff` |

The `0b` and `0x` prefixes show which base the result uses. `bin()` converts an integer to a binary string, and `hex()` converts it to a hexadecimal string. Python uses lowercase letters for hexadecimal digits in these results.

### Task 5.4 - How text and data are stored

The ASCII decimal code for uppercase `A` is 65, and for lowercase `a` it is 97. An encoding gives characters number values so a computer can store and read text consistently. UTF-8 can represent many characters beyond basic ASCII; for example, `₹` is not in basic ASCII.

A bit is one binary digit, either 0 or 1. Eight bits make one byte. Using binary data units, 1 KiB is 1,024 bytes, 1 MiB is 1,024 KiB, and 1 GiB is 1,024 MiB.

## 3. Commands / tools used

- `python3` - opened the Python prompt to check conversion expressions.
- `python3 mission-05-numbers-data/number_converter.py` - ran the converter. I supplied 18, 42 and 255 as inputs.
- `bin()` - converted an integer to a binary string.
- `hex()` - converted an integer to a hexadecimal string.
- `int(value, base)` - read a string as a number in the given base, such as `int('1010', 2)`.
- `input()` and `print()` - read the decimal number and show the converted results.

## 4. My understanding

Decimal uses ten digits, binary uses two, and hexadecimal uses sixteen. In binary, each position is a power of 2. Hexadecimal is shorter to write than binary because one hex digit represents four binary bits; for example, `1111₂` is `F₁₆`.

The converter stores the typed value in the `number` variable after `int()` changes the input text into an integer. Then `bin()` and `hex()` make strings that `print()` displays. The program is kept simple and expects a valid decimal integer, so a word or an empty response would not convert.

## 5. Difficulties faced

When checking binary `1010`, I first typed `int('1010')`. Python returned 1010, which did not match my expected answer. I had forgotten that `int()` assumes decimal if I do not tell it the base.

## 6. How I resolved them

I added the base as the second argument: `int('1010', 2)`. Python then returned 10, which matched my hand calculation. I also kept the `0b` and `0x` prefixes in the converter output so I could tell the bases apart.

## 7. Evidence / files

- `number_converter.py` - the working decimal-to-binary and decimal-to-hexadecimal program.
- This README - manual conversions, Python checks, the three program results, and notes on encoding and data sizes.
- No personal Mac details are included.

## 8. Commit details

- Commit message: `Build number converter and practise data representation`
- Status: committed locally on `main`; not pushed to GitHub.
