
---

# Ball Wall Game

This repository contains the code for **Ball Wall**, a simple game built using an **Arduino**, an **OLED display**, and **button inputs**. The game allows the player to move a ball within a bounded area on the OLED screen, controlled by directional buttons. This project is a fun way to learn about graphical rendering, button inputs, and basic game mechanics on microcontrollers.

---

## Features
- Displays a movable ball on a 128x64 OLED screen.
- Uses directional buttons to control the ball's movement (Up, Down, Left, Right).
- Includes boundary checks to restrict the ball's movement within a predefined area.

---

## Components
1. **Arduino Board**  
   Compatible with Arduino Uno, Nano, Mega, etc.

2. **OLED Display**  
   128x64 resolution with SSD1306 driver (I2C communication).

3. **Buttons (x4)**  
   Used for directional input (Up, Down, Left, Right).

4. Miscellaneous:
   - Breadboard
   - Jumper wires

---

## Circuit Diagram
Connect the components as shown below:

| Component  | Arduino Pin   |
|------------|---------------|
| OLED SDA   | A4 (I2C SDA)  |
| OLED SCL   | A5 (I2C SCL)  |
| Right Button | D2           |
| Left Button  | D3           |
| Up Button    | D4           |
| Down Button  | D5           |
| Power (VCC) | 5V           |
| Ground (GND)| GND          |

> Ensure the buttons are configured with pull-up resistors or use the `INPUT_PULLUP` setting in the code.

---

## Libraries Used
- [U8g2 Library](https://github.com/olikraus/u8g2)  
  For controlling the OLED display and rendering graphics.

- [Wire Library](https://www.arduino.cc/en/Reference/Wire)  
  Built into Arduino for I2C communication.

---

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/ball-wall-game.git
   cd ball-wall-game
   ```
2. Install the required libraries via Arduino IDE:
   - Open **Library Manager** (`Sketch > Include Library > Manage Libraries...`).
   - Search for "U8g2" and install the library.

3. Open the `ball_wall.ino` file in the Arduino IDE.

---

## Usage
1. Wire the components as described in the circuit diagram.
2. Upload the code to your Arduino board.
3. Control the ball using the directional buttons:
   - **Up, Down, Left, Right** to move the ball.
4. The ball moves within a predefined boundary displayed on the OLED screen.

---

## Customization
- **Change boundaries**: Modify the `bounds[]` array to adjust the allowed movement area.
- **Speed adjustment**: Increase or decrease the movement speed by adjusting the `img[]` update values in the code.
- **Graphics**: Replace `image_Pressed_Button_13x13_bits` with custom bitmap graphics for a different ball design.

---

## Contributing
Contributions to improve this game or expand its functionality are welcome! Feel free to fork the repository, add features, and submit a pull request.

---

## License
This project is licensed under the MIT License. See `LICENSE` for more details.

---
