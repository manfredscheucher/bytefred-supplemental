# Binary adder verification

Verifies the logic of a binary adder, by bruteforce and with the SMT solver z3.
The adder itself is shown on a breadboard in [this video](https://youtube.com/shorts/Wp9NyUa-Dh4).

| Script | Verifies | Method |
| --- | --- | --- |
| `bruteforce-2bit.py` | 2-bit adder | tries all inputs |
| `smt-2bit.py` | 2-bit adder | z3 |
| `smt-kbit.py` | k-bit adder | z3 |

## Run

The SMT scripts need z3:

```bash
pip install z3-solver
```

```bash
python3 bruteforce-2bit.py
python3 smt-2bit.py
python3 smt-kbit.py 8
```

The argument of `smt-kbit.py` is the number of bits.

Bruteforce runtime grows exponentially with the number of input bits, so it doesn't scale to larger circuits. The SMT scripts handle larger setups easily.
