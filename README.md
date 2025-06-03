# 🕹️ Arduino Reaction Game

This is a simple two-player reaction game built using an **Arduino**, an **I2C LCD display**, two **buttons**, and two **LEDs**. Players compete to react fastest after a countdown, while avoiding pressing their button too early.

---

## 🎮 Game Overview

- Each round starts when **both players press their buttons simultaneously**.
- The game has **5 rounds**.
- LEDs light up and turn off with **random delays**.
- Once **both LEDs turn off**, players race to press their buttons.
- Pressing **too early** (before LEDs turn off) awards a point to the other player.
- The player with the **highest score after 5 rounds** wins.

---

## 🧰 Components Used

| Component        | Quantity |
|------------------|----------|
| Arduino Uno      | 1        |
| Push Buttons     | 2        |
| LEDs             | 2        |
| 220Ω Resistors   | 2        |
| LiquidCrystal I2C LCD (16x2) | 1 |
| Jumper Wires     | Several  |
| Breadboard       | 1        |

---

## 🔌 Wiring

| Arduino Pin | Component        |
|-------------|------------------|
| D2          | Button 1         |
| D3          | Button 2         |
| D4          | LED 1            |
| D5          | LED 2            |
| I2C (A4/A5) | LCD SDA/SCL      |

Make sure to include appropriate pull-down resistors or use the internal pull-up/pull-down configurations for button stability.

---

## 💻 How to Use

1. **Upload the code** to your Arduino using the Arduino IDE.
2. **Power on** the board.
3. LCD will display: `Start Game` / `Press both btns`.
4. Players press both buttons to start.
5. Follow the countdown and try to press your button first after the LEDs turn off.
6. The LCD shows round winner and score updates.
7. Game ends after 5 rounds with a final winner announcement.

---

## 📂 Code Structure

- `setup()` initializes LCD, buttons, and LEDs.
- `loop()` waits for both players to start.
- `playRound()` handles LED countdown, early presses, and winner detection.
- `debounceButton()` ensures stable button reads.
- `updateDisplay()` and `displayScores()` handle LCD output.

---
