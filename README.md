# 🍽️ Restaurant Table Booking Simulation

An **agent-based simulation** of a restaurant table booking system built with **Python**, **Mesa**, and **Solara**. Customers arrive, look for available tables that fit their group size, preferred time slot, **and preferred table zone**, then either get seated or join a waiting list.

---

## 📸 Screenshots


### Web Interface
<img width="1852" height="865" alt="B1" src="https://github.com/user-attachments/assets/9fd1207d-733c-49f6-88bb-eb4ef6b221e1" />


### Restaurant Grid
<img width="1835" height="850" alt="B2&#39;1" src="https://github.com/user-attachments/assets/7ce07756-e6e4-484a-8eb2-09978544d698" />
<img width="1847" height="876" alt="B2&#39;2" src="https://github.com/user-attachments/assets/ddb0fcaf-c2cf-4db9-93c6-c56571a14b7e" />


---

## ✨ Features

| # | Feature | Description |
|---|---------|-------------|
| 1 | **Agent-Based Customers** | Each customer has a unique ID, group size (2, 4, or 6), preferred time slot, and table preference |
| 2 | **Multiple Time Slots** | 6:00 PM, 7:00 PM, 8:00 PM, 9:00 PM – customers book for a specific time |
| 3 | **Table Preferences** | Customers can prefer: 🪟 Window, 🚪 Door, or 📍 Center tables |
| 4 | **Table Management** | Tables of sizes 2, 4, and 6 are placed in the restaurant grid with zone labels |
| 5 | **Waiting List** | Customers who can't find a table join a waiting list and try again next step |
| 6 | **Data Collection** | Tracks occupied tables, waiting customers, and bookings per time slot |
| 7 | **Color-Coded Visualization** | Purple (6:00 PM), Cyan (7:00 PM), Magenta (8:00 PM), Gold (9:00 PM) |
| 8 | **Interactive Web Interface** | Solara-based UI with sliders for all parameters |
| 9 | **Gray Transparent Sidebar** | Modern frosted glass effect with blur |

---

## 🎯 What This Simulation Does

1. **Customers arrive** at the restaurant with a random group size (2, 4, or 6 people).
2. Each customer is assigned a **random time slot** (6:00 PM, 7:00 PM, 8:00 PM, or 9:00 PM).
3. Each customer has a **random table preference**:
   - 🪟 **Window** – wants a table near the edge
   - 🚪 **Door** – wants a table near the entrance
   - 📍 **Center** – wants a table in the middle
4. Customers look for an **empty table** that:
   - Can fit their group size
   - Is in their **preferred zone**
   - Is empty for their time slot
5. If a matching table is available, they book it.
6. If no matching table is available, they join the **waiting list**.
7. Waiting customers **try again** in the next simulation step.
8. The **DataCollector** records:
   - Number of occupied tables
   - Number of waiting customers
   - Bookings for each time slot (6:00 PM, 7:00 PM, 8:00 PM, 9:00 PM)
9. The **grid** shows:
   - Tables as colored rectangles with zone labels (W = Window, D = Door, C = Center)
   - Customers as colored dots (purple = 6:00 PM, cyan = 7:00 PM, magenta = 8:00 PM, gold = 9:00 PM, red = waiting)

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| **Python 3.11+** | Programming language |
| **Mesa** | Agent-based modeling framework |
| **Matplotlib** | Grid visualization |
| **Solara** | Interactive web interface |
| **NumPy / Pandas** | Data collection and analysis |
| **HTML / CSS** | UI styling (via Solara) |

---

## 🚀 How to Run

### 1️⃣ Install Dependencies

Open your terminal (Command Prompt, PowerShell, or Anaconda Prompt) and run:

```bash
pip install mesa solara matplotlib numpy pandas
