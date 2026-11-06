# Snake game with Arduino

Snake in the terminal, controlled with a breadboard controller through an Arduino, as shown in [this video](https://www.youtube.com/shorts/PYbnNydN6qM).

| File | Purpose |
| --- | --- |
| `arduino-controller.ino` | runs on the Arduino, sends A0, A1, A2, A3 (up, left, right, down) over serial |
| `test-controller.py` | prints the pressed directions, to check the controller |
| `snake-game.py` | the game |

## Run

1. Upload `arduino-controller.ino` to the Arduino. The Arduino IDE will offer to move it into a folder of the same name, which is fine.

2. Install pyserial:

   ```bash
   pip install pyserial
   ```

3. Optionally check the controller:

   ```bash
   python3 test-controller.py
   ```

4. Start the game:

   ```bash
   python3 snake-game.py
   ```

Both Python scripts expect the Arduino on `/dev/ttyACM0`. To use another port, change it in the script.
