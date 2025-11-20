# 📚 STUDENT MANAGEMENT SYSTEM  
A Complete Python-Based Academic & Scheduling Manager

The **Student Management System (SMS)** is a fully functional academic data handler written in Python.  
It manages students, faculty, courses, grades, tasks, schedules, and faculty–course relationships using CSV-based storage.

This project provides a robust structural backend for academic institutions, eliminating manual tracking and enabling automated workflows for evaluation, attendance, grading, task management, and test scheduling.

---

## ✨ Features

### 🎓 Student Management
- Add new students  
- View all students  
- Track academic details  
- Update records  

### 👨‍🏫 Faculty Management
- Add faculty  
- Assign faculty to courses  
- View faculty–course mappings  

### 📘 Course Management
- Add courses  
- Map students to courses  
- Maintain course metadata  

### 📝 Marks & Performance Tracking
- Add/update marks  
- Store evaluation records  
- Automatic saving to CSV  

### 🗓 Test Scheduling
- Create test schedules  
- Store date, time, course, faculty  
- Prevent duplicate booking  

### 🧾 Task Management
- Add tasks  
- Track deadlines  
- Manage task list for each student  

### 📂 CSV-Based Database
- No SQL needed  
- Everything stored in structured CSV files  
- Easy export/import  

---

## 🏗 Project Structure

```
sms/
└── Student_Management_System-main/
    ├── F13CPSlabeval3.py           # Main executable
    │
    ├── student_info.csv             # Student records
    ├── course_info.csv              # Course list
    ├── student_marks.csv            # Marks data
    ├── faculty_info.csv             # Faculty list
    ├── faculty_course_info.csv      # Mapped teaching courses
    ├── tasks.csv                    # Student Tasks
    ├── test_schedule.csv            # Exam schedules
    │
    └── README.md
```

---

## 🧩 System Architecture

```
┌───────────────────────────────┐
│      Student Manager          │
└───────────────┬───────────────┘
                │
┌───────────────▼───────────────┐
│      Course Manager           │
└───────────────┬───────────────┘
                │
┌───────────────▼───────────────┐
│      Faculty Manager          │
└───────────────┬───────────────┘
                │
┌───────────────▼───────────────┐
│      Marks Manager            │
└───────────────┬───────────────┘
                │
┌───────────────▼───────────────┐
│      Test Scheduler           │
└───────────────┬───────────────┘
                │
┌───────────────▼───────────────┐
│      Task Manager             │
└───────────────────────────────┘
```

Everything interacts through **CSV data pipelines**, making the system lightweight and fast.

---

## 📦 Included CSV Files

### 1. **student_info.csv**
| student_id | name | branch | year |
|------------|------|--------|------|

### 2. **course_info.csv**
| course_id | course_name | credits |
|-----------|-------------|---------|

### 3. **faculty_info.csv**
| faculty_id | name | department |
|------------|------|------------|

### 4. **student_marks.csv**
| student_id | course_id | marks |
|------------|-----------|-------|

### 5. **faculty_course_info.csv**
| faculty_id | course_id |
|------------|-----------|

### 6. **tasks.csv**
| student_id | task | deadline | status |
|------------|------|----------|--------|

### 7. **test_schedule.csv**
| date | time | course_id | faculty_id |
|------|------|-----------|------------|

---

## ⚙️ Installation

### 1. Extract the ZIP
```bash
unzip Student_Management_System-main.zip
cd Student_Management_System-main
```

### 2. Ensure Python3 is installed
```bash
python --version
```

No external libraries required—pure Python + CSV.

---

## ▶️ Running the System

Run the main script:

```bash
python F13CPSlabeval3.py
```

This opens the CLI menu.

---

## 🖥 CLI Menu (Example)

```
1. Add Student
2. View Students
3. Add Course
4. View Courses
5. Add Faculty
6. Map Faculty to Course
7. Add Marks
8. View Marks
9. Add Task
10. Schedule Test
11. View Test Schedule
12. Exit
```

---

## 🔍 How Each Module Works

### 1. Student Module
- Adds new students
- Stores into `student_info.csv`
- Auto-generates student IDs

### 2. Faculty Module
- Adds faculty
- Stores in `faculty_info.csv`

### 3. Course Module
- Courses stored in `course_info.csv`

### 4. Mapping Faculty <-> Course
- Stored in `faculty_course_info.csv`

### 5. Marks Module
- Add/update marks
- Stored in `student_marks.csv`

### 6. Task Manager
- Add tasks
- Tracks completion
- Stores in `tasks.csv`

### 7. Test Scheduler
- Date, time, course, faculty
- Stored in `test_schedule.csv`
- Avoids conflicts

---

## 📈 Data Flow Overview

```
User Input
   │
   ▼
CLI Menu
   │
   ├── Student → student_info.csv
   ├── Course → course_info.csv
   ├── Faculty → faculty_info.csv
   ├── Marks → student_marks.csv
   ├── Tasks → tasks.csv
   └── Test Schedule → test_schedule.csv
```

---

## 🧪 Example CSV Entries

### student_info.csv
```
1,Sharvesh,CSE,1
2,Akhil,EEE,2
```

### course_info.csv
```
CS101,Python Programming,4
CS102,Data Structures,3
```

### test_schedule.csv
```
2025-01-29,10:00,CS101,FC01
```

---

## 🚀 Future Enhancements

- Convert CSV → SQLite or MySQL
- GUI using PyQt or Tkinter
- Faculty login & student login
- Attendance tracking
- Analytics dashboard
- Auto-grade calculation
- Web UI (Django/Flask)

---

## 🤝 Contribution

1. Fork
2. Create feature branch
3. Commit & push
4. Submit PR

---

## 📄 License

This project is free to use for education and development purposes.

---

## 🙏 Acknowledgements

- Python CSV module
- Academic scheduling logic
- Data-management design concept
