# 🎓 Student Life Simulator (Mobile Edition)

A **text-based life simulation game written in C** where you must survive 5 intense days of student life. Balance your **Productivity, Energy, Happiness, and Stress** to achieve the ultimate title:

> 🏆 **"Academic Weapon"**

---

## 🚀 Features

### 🔄 Dynamic Attribute System

Manage four core stats:

* 📚 Productivity
* ⚡ Energy
* 😊 Happiness
* 😰 Stress

Every decision impacts your survival.

---

### 🔥 Burnout Mechanics

* If **Stress ≥ 100** OR **Energy = 0**
* You are **forced to rest**, skipping a turn

---

### 📈 Study Streak System

* Consecutive studying rewards you with:

  * ➕ **+10 bonus Productivity**
* Encourages discipline and consistency

---

### ⚡ Adaptive Difficulty

Each day introduces unique modifiers:

* 😵 *Monday Blues* → Higher stress
* 🚨 *DEADLINE PANIC!* → Increased pressure & rewards

---

### 💾 Persistent Save System

Game automatically saves to:

```
student_data.txt
```

Includes:

* Player Name
* Current Stats
* Day Progress
* Action History

---

### 🎮 Gameplay Modes

* ⚡ **Speedrun Mode** → Play all 5 days instantly
* 🕒 **Realism Mode** → 24-hour cooldown between days

---

## 🎮 How to Play

### 📅 Daily Actions

Choose **ONE action per day**:

| Action           | Productivity   | Energy | Happiness | Stress |
| ---------------- | -------------- | ------ | --------- | ------ |
| 📚 Study         | +20 (variable) | -20    | -5        | +10    |
| 📱 Reels         | 0              | -10    | +8        | -5     |
| 🎮 Game          | 0              | -15    | +15       | -10    |
| 😴 Sleep         | -5             | +30    | 0         | -8     |
| 🧑‍🤝‍🧑 Hangout | -8             | -20    | +20       | +5     |

---

## 🏆 Winning Condition

Maintain:

```
Average Productivity ≥ 75
```

to achieve:

* 🎓 Grade B or higher
* 🏅 "Academic Weapon" status

---

## 📊 End-Game Analysis

At the end of Day 5, receive your **Final Report Card**:

### 📉 Visual Recap

* Bar chart of daily productivity

### 😬 Regret Score

* Based on:

  * Final Stress
  * Happiness
  * Academic Performance

### 🧠 Identity Tags

Your playstyle defines you:

* 🏆 Academic Weapon
* 🤫 Quiet Grinder
* 😱 Panic Master
* 🔥 Burnt Out

---

## 🎲 Random Events

* 33% chance each day
* Examples:

  * Surprise assignments 📄
  * Friend interactions 🧑‍🤝‍🧑
  * Unexpected stress boosts 😬

---

## 🛠️ Technical Details

* **Language:** C
* **Data Handling:** File I/O (`student_data.txt`)
* **Randomness:** `rand()` for dynamic events
* **Portability:** Works on:

  * Windows
  * Linux / Unix

Includes:

* Cross-platform screen clearing functions
* Structured modular design

---

## 📂 Project Structure (Example)

```
📁 Student-Life-Simulator
│── main.c
│── game_logic.c
│── save_system.c
│── student_data.txt
│── README.md
```

---

## 💡 Future Improvements

* 🎯 Skill Tree System
* 📅 Weekly Planning Mode
* 🧠 Advanced Mental Health Mechanics
* 🖥️ Improved Terminal UI (ASCII Graphics)

---

## 🧑‍💻 Author

Developed as a **C programming project** combining:

* Game logic
* File handling
* Simulation design

---

## ⭐ Contribute

Feel free to:

* Fork the repo
* Improve features
* Add new events or mechanics

---

## 📜 License

This project is open-source and free to use for learning purposes.

---

> 💬 *"Balance your life before it balances you."*
