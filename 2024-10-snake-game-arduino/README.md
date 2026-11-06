# Snake game with Arduino

Snake in the terminal, controlled with a breadboard controller through an Arduino, as shown in [this video](https://www.youtube.com/shorts/PYbnNydN6qM).

## Run

The game needs pyserial:

```bash
pip install pyserial
```

```bash
python3 snake-game.py
```

The game expects an Arduino on `/dev/ttyACM0` at 9600 baud, sending the analog values of A0, A1, A2 and A3 (up, left, right, down) as one line of space-separated numbers. To use another port, change it in the script.

## Tests

- `tests/test1-arduino.ino`: Arduino sketch, sends the values of A0, A1, A2 and A3 over serial
- `tests/test2-python-interface.py`: reads these values and prints the pressed directions
