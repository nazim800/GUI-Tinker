# 🏋️‍♂️ Smart Fitness Management System (SFMS)

A Python-based application built using Object-Oriented Programming (OOP) principles and enhanced with a **Tkinter GUI interface** to manage gym and fitness center operations. This version of SFMS offers both command-line and graphical interaction, designed to streamline user management, workout tracking, nutrition logging, and goal progress monitoring.

---

## 📌 Project Overview

With digital transformation reshaping the fitness industry, the **Smart Fitness Management System (SFMS)** bridges traditional gym workflows with modern software solutions. Built for gym operators, fitness professionals, and individuals, it supports:

* Member and trainer registration
* Fitness class scheduling
* Workout and nutrition logging
* Progress tracking and analytics
* Dual-interface design (CLI + Tkinter GUI)

---

## 🖼️ System Design & GUI Layout Overview

The system offers a **dual-interface** approach:

* **CLI**: Handles basic operations with terminal input.
* **GUI (Tkinter)**: Offers a user-friendly, tabbed layout using `ttk.Notebook` for modular navigation.

Each tab corresponds to a feature area:

* User Management
* Workout Logging
* Goal Tracking
* Nutrition
* Reports

GUI elements include `Entry`, `Label`, `Button`, and `Text`, designed for clarity, usability, and future extensibility.

---

## ✨ Features and Functions

* **User Management**: Register, update, list, and delete profiles with fitness goals.
* **Workout Logging**: Track type, duration, calories, and notes.
* **Progress Report**: Calculate progress based on calories burned vs. goal.
* **Nutrition Tracking**: Log meals and calorie intake.
* **Reports & Analytics**: Summary of fitness and nutrition performance.

> Built with modularity in mind—future features like meal planning or data export can be easily added.

---

## 🐛 Issues & Solutions

| Challenge            | Solution                                                               |
| -------------------- | ---------------------------------------------------------------------- |
| Dual-interface logic | Conditional interface loader in `main()`                               |
| Input validation     | Used basic `if-else`, error trapping, and message boxes; regex pending |
| Data storage         | Current use of in-memory dictionaries; JSON/SQLite proposed            |

---

## 🧪 Testing Results

| Scenario              | Status    | Description                                              |
| --------------------- | --------- | -------------------------------------------------------- |
| New User Registration | ✅ Success | Profile added to dictionary and confirmed                |
| Workout Logging       | ✅ Success | User workouts appended with date, calories, and type     |
| Progress Calculation  | ✅ Success | Percentage of goal achieved displayed                    |
| Error Handling        | ✅ Passed  | GUI properly alerts when invalid input or user not found |

> The GUI walks users through all actions with clear labels and input validation.

---

## 💻 Sample GUI Code (Tkinter-based)

```python
import tkinter as tk
from tkinter import messagebox, ttk
from datetime import datetime

user_data = {}  # In-memory store for testing

class SFMSApp(tk.Tk):
    def __init__(self):
        super().__init__()
        self.title("Smart Fitness Management System")
        self.geometry("850x600")
        self.tabs = ttk.Notebook(self)
        self.tabs.pack(expand=1, fill="both")

        self.create_user_management()
        self.create_workout_tracking()
        self.create_goal_tracking()
        self.create_nutrition_tracking()
        self.create_reports_interface()

    def create_user_management(self):
        # Setup user management UI tab
        pass

    def create_workout_tracking(self):
        # Setup workout logging UI tab
        pass

    def create_goal_tracking(self):
        # Setup goal tracking and progress monitor
        pass

    def create_nutrition_tracking(self):
        # Setup meal logging and nutrition analysis
        pass

    def create_reports_interface(self):
        # Setup summary reports and feedback
        pass

if __name__ == "__main__":
    app = SFMSApp()
    app.mainloop()
```

---

## 📸 GUI Preview

> User Management tab

<img width="468" alt="image" src="https://github.com/user-attachments/assets/59a105ff-e4f1-4b16-98e3-e6d6e0d1d090" />

> Workout Tracker

<img width="468" alt="image" src="https://github.com/user-attachments/assets/f27c38a3-9c9a-48d1-972f-0857908f201f" />

<img width="468" alt="image" src="https://github.com/user-attachments/assets/63a5373e-1a63-483f-be36-b90dc5d047f7" />

<img width="396" alt="image" src="https://github.com/user-attachments/assets/06f0565d-b6a6-452c-b31a-84db59b17abd" />



> Reports interface

<img width="468" alt="image" src="https://github.com/user-attachments/assets/88e6d369-49ca-4e11-ab15-92383b674c83" />


---

## 🧠 Conclusion

The **Smart Fitness Management System** demonstrates modular architecture and clean coding principles with GUI support. Developed as part of **ICT701 Assessment 4**, it supports future scalability with features like database integration, user authentication, and advanced analytics.

> 🚀 *This project exemplifies practical application of OOP, event-driven design, and GUI development in Python.*
