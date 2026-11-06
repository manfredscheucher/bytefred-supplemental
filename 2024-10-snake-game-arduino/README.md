# Snake game with Arduino

Snake in the terminal, controlled with a breadboard controller through an Arduino, as shown in [this video](https://www.youtube.com/shorts/PYbnNydN6qM).

## Run

1. Upload `test1_arduino_IDE/test1_arduino_IDE.ino` to the Arduino. It sends the analog values of A0, A1, A2 and A3 (up, left, right, down) over serial.

2. Install pyserial:

   ```bash
   pip install pyserial
   ```

3. Optionally check the controller. This prints the pressed directions:

   ```bash
   python3 test2_python_interface/test2_python_interface.py
   ```

4. Start the game:

   ```bash
   python3 snake-game.py
   ```

Both Python scripts expect the Arduino on `/dev/ttyACM0`. To use another port, change it in the script.
