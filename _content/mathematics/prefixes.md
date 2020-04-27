---
title: Metric & Binary Prefixes
description: Uni, Bi, Kilo, Mibi etc.
author: ibraheem_rodrigues
---

| Metric Prefix[^1] | Symbol | Factor | Factor | Symbol | Metric Prefix |
|-|-|-|-|-|-|
| Yotta | Y  | $$ 10^{24} $$ | $$ 10^{-24} $$ | y | Yocto | 
| Zetta | Z  | $$ 10^{21} $$ | $$ 10^{-21} $$ | z | Zepto | 
| Exa   | E  | $$ 10^{18} $$ | $$ 10^{-18} $$ | a | Atto  | 
| Peta  | P  | $$ 10^{15} $$ | $$ 10^{-15} $$ | f | Femto | 
| Tera  | T  | $$ 10^{12} $$ | $$ 10^{-12} $$ | p | Pico  | 
| Giga  | G  | $$ 10^{9} $$  | $$ 10^{-9} $$  | n | Nano  | 
| Mega  | M  | $$ 10^{6} $$  | $$ 10^{-6} $$  | µ | Micro | 
| Kilo  | k  | $$ 10^{3} $$  | $$ 10^{-3} $$  | m | Milli | 
| Hecto | h  | $$ 10^{2} $$  | $$ 10^{-2} $$  | c | Centi | 
| Deca  | da | $$ 10^{1} $$  | $$ 10^{-1} $$  | d | Deci  |

When used to denote a number of bits/bytes (kilobyte, megabit, etc.), there is some ambiguity as whether these units refer to a multiple of $$ 10^{3} = 1000 $$, as above, or a multiple of $$ 2^{10} = 1024 $$. The IEC defines the following **Binary Prefixes** in an attempt to alleviate this issue, although adoption is ultimately implementation dependent.

| Binary Prefix[^2] | Symbol | Factor |
|-|-|-|
| Yobi | Yi | $$ 2^{80} $$ |
| Zebi | Zi | $$ 2^{70} $$ |
| Exbi | Ei | $$ 2^{60} = 1152921504606846976 $$ |
| Pebi | Pi | $$ 2^{50} = 1125899906842624 $$ |
| Tebi | Ti | $$ 2^{40} = 1099511627776 $$ |
| Gibi | Gi | $$ 2^{30} = 1073741824 $$  |
| Mebi | Mi | $$ 2^{20} = 1048576 $$  |
| Kibi | Ki | $$ 2^{10} = 1024 $$  |


[^1]: [https://www.bipm.org/en/measurement-units/](https://www.bipm.org/en/measurement-units/) Accessed 27/04/2020.
[^2]: [https://physics.nist.gov/cuu/Units/binary.html](https://physics.nist.gov/cuu/Units/binary.html) Accessed 27/04/2020.
