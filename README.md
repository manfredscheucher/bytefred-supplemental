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

## 2024-10-snake-game-arduino

Snake in the terminal, controlled with a breadboard controller through an Arduino, as shown in [this video](https://www.youtube.com/shorts/PYbnNydN6qM).

The script needs pyserial:

```bash
pip install pyserial
```

Run from inside the folder:

```bash
python3 snake-game.py
```

The script expects the Arduino on `/dev/ttyACM0` at 9600 baud, sending the analog values of A0, A1, A2 and A3 (up, left, right, down) as one line of space-separated numbers. To use another port, change it in the script.
