# ByteFred supplemental

Supplemental source code for ByteFred videos, one folder per topic.

## 2024-11-binary-adder-verification

Verifies the logic of a binary adder, by bruteforce and with the SMT solver z3.
The adder itself is shown on a breadboard in [this video](https://youtube.com/shorts/Wp9NyUa-Dh4).

| Script | Verifies | Method |
| --- | --- | --- |
| `python-bruteforce.py` | 2-bit adder | tries all inputs |
| `python-SMT-2bit.py` | 2-bit adder | z3 |
| `python-SMT-kbit.py` | k-bit adder | z3 |

The SMT scripts need z3:

```bash
pip install z3-solver
```

Run from inside the folder:

```bash
python3 python-bruteforce.py
python3 python-SMT-2bit.py
python3 python-SMT-kbit.py 8
```

The argument of `python-SMT-kbit.py` is the number of bits.
Bruteforce runtime grows exponentially with the number of input bits, so it doesn't scale to larger circuits.
