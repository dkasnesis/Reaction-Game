# 🕹️ Arduino Reaction Game

A fast-paced two-player reaction game built with Arduino. Players race to press their button after a random countdown — but if they press too soon, the point goes to the other player! The game includes a 16x2 LCD for live feedback, scorekeeping, and round updates.

---

## 🚀 Features

- ⏱️ **5 Rounds of Play**
- ⚡ **Randomized Countdown**
- 🚫 **Early Press Detection**
- 📺 **Live Score Display via I2C LCD**
- 🧠 **Button Debouncing Logic**
- 🧩 **Easy-to-Build with Basic Components**

---

## 🎮 How It Works

1. Both players press their buttons simultaneously to begin.
2. LEDs light up and shut off one-by-one with random delays.
3. When all LEDs are off, players must react quickly and press their buttons.
4. The first to press after the LEDs turn off wins the round.
5. Pressing **too early** (while LEDs are on) gives the point to the opponent.
6. After 5 rounds, the LCD displays the final winner.

---

## 🧰 Hardware Required

| Component                 | Quantity |
|---------------------------|----------|
| Arduino Uno (or similar)  | 1        |
| Push Buttons              | 2        |
| LEDs                      | 2        |
| 220Ω Resistors            | 2        |
| I2C LCD Display (16x2)    | 1        |
| Breadboard & Jumper Wires | As needed |

---

## 🔌 Wiring Overview

| Arduino Pin | Component        |
|-------------|------------------|
| D2          | Button 1         |
| D3          | Button 2         |
| D4          | LED 1            |
| D5          | LED 2            |
| A4 (SDA)    | LCD SDA          |
| A5 (SCL)    | LCD SCL          |

Use pull-down resistors for buttons, or configure internal pull-up/down as needed.

---

## 💻 Getting Started

1. Clone this repo or copy the `.ino` file into your Arduino IDE.
2. Make sure the **I2C LCD address** (`0x27`) matches your display. Adjust if necessary.
3. Upload the code to your Arduino board.
4. Open the Serial Monitor (9600 baud) to see debug logs.
5. Power on, and follow the instructions shown on the LCD.

---

## 🧠 Code Highlights

- **Debounce Logic:** Ensures stable button reads.
- **LCD Updates:** Displays round messages, live scores, and winner.
- **Randomized Delays:** Each LED turns off at different random intervals.
- **Game Looping:** Game resets automatically after completion.

---

## 📺 LCD Output Example

Round 3
P1:2 P2:1

Player 2 Early
P1:3 P2:1

End Game
P1:4 P2:1
---

## 🛠️ Customization Ideas

- Add a **buzzer** for sound feedback.
- Store **high scores** using EEPROM.
- Use **RGB LEDs** for visual effects.
- Extend game modes for more players or different rules.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🤝 Contributing

Got ideas for improvements or want to add new features? PRs and issues are welcome!

---

## 📷 Optional: Demo

> Add a GIF or YouTube link here showing gameplay and LCD output  
> Example: ![Gameplay Demo](link-to-your-gif-or-video)

---

