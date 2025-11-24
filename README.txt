# 📅 Teacher–Student Scheduler & Task Manager

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
