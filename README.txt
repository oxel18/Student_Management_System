<h1>📅 Teacher–Student Scheduler & Task Manager<h1>

A Python GUI project that connects a **Teacher Test Scheduler** with a **Student Task Manager** using shared CSV files. Teachers schedule tests only in valid class periods, and students view those tests along with their own tasks on a calendar.

---

## ✨ What It Does

- Teacher side:
  - Select faculty and subject.
  - Pick a future date from a calendar.
  - See only valid periods from the official timetable.
  - Save scheduled tests to `test_schedule.csv`.

- Student side:
  - Add personal tasks (title, date, priority, status).
  - Load tests from `test_schedule.csv` into the task list.
  - View tasks/tests for any selected date.
  - Save all tasks to `tasks.csv`.

---

## 🗂 Files

- `F13CPSlabeval3.py` – Main Python file (teacher & student GUIs).
- `faculty_course_info.csv` – Faculty and course mapping.
- `class_timetable.csv` – Weekly timetable with days, slots, and subjects.
- `test_schedule.csv` – Tests scheduled by teachers.
- `tasks.csv` – Student task storage.
- `README.md` – Project description.

---

## ⚙️ Requirements

- Python 3.8+
- Tkinter (bundled with Python)
- Install extra libraries:

pip install tkcalendar pandas

---

## 🚀 How to Run

1. Make sure all CSV files are in the same folder as `F13CPSlabeval3.py`.
2. Run:

3. In the terminal prompt:
   - Type `t` for **Teacher interface**.
   - Type `s` for **Student interface**.
   - Type `e` to **exit**.

---

## 👩‍🏫 Teacher Interface

- Choose your name from the faculty dropdown.
- Choose one of your subjects.
- Select a **future** date from the calendar.
- Click button to **load available periods** (from timetable).
- Select a period and confirm to save into `test_schedule.csv`.

---

## 👨‍🎓 Student Interface

- Existing tasks are loaded from `tasks.csv` (if present).
- Add a task by entering:
  - Title  
  - Date (`YYYY-MM-DD`)  
  - Priority (e.g., High/Medium/Low)  
  - Status (e.g., Pending/Done)
- Click **Add Task** to save it.
- Click **Update Schedule** to import tests from `test_schedule.csv`.
- Click a calendar date and use **Check Tasks for Selected Dates** to see tasks/tests for that day.

---

## 🔮 Future Ideas

- Color‑coded calendar events.
- Drop‑down status selector.
- Export upcoming tasks/tests to PDF or CSV.
- Simple login for multiple teachers/students.

