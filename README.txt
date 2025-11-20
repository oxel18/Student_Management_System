# 📚 STUDENT MANAGEMENT SYSTEM

A Complete Python-Based Academic & Scheduling Manager

**Student Management System (SMS)** is a fully functional academic data handler built with Python. It manages students, faculty, courses, grades, tasks, schedules, and faculty–course relationships using CSV-based storage.

This project provides a robust structural backend for academic institutions, eliminating manual tracking and enabling automated workflows for evaluation, attendance, grading, task management, and test scheduling.

---

## ✨ Features

### 🎓 Student Management
- **Add New Students** – Register students with ID, name, branch, and year
- **View All Students** – Display complete student roster
- **Track Academic Details** – Monitor student progress and records
- **Update Records** – Modify existing student information

### 👨‍🏫 Faculty Management
- **Add Faculty** – Register faculty with ID, name, and department
- **Assign to Courses** – Map faculty members to courses they teach
- **View Mappings** – Display faculty–course relationships
- **Department Tracking** – Organize faculty by departments

### 📘 Course Management
- **Add Courses** – Create new courses with ID, name, and credits
- **Map Students** – Enroll students in courses
- **Course Metadata** – Track credits, prerequisites, and descriptions
- **View Course List** – Display all available courses

### 📝 Marks & Performance Tracking
- **Add/Update Marks** – Record student grades for courses
- **Evaluation Records** – Store assessment results
- **Performance Reports** – Generate grade summaries
- **Automatic CSV Saving** – Persistent data storage

### 🗓 Test Scheduling
- **Create Test Schedules** – Plan exams with date, time, course
- **Faculty Assignment** – Link faculty to scheduled tests
- **Conflict Prevention** – Avoid duplicate bookings
- **Calendar View** – Display upcoming tests

### 🧾 Task Management
- **Add Tasks** – Create assignments and tasks
- **Track Deadlines** – Monitor due dates
- **Status Updates** – Mark tasks as complete/incomplete
- **Student Task Lists** – Personal task management

### 📂 CSV-Based Database
- **No SQL Required** – Lightweight file-based storage
- **Structured Data** – Clean CSV format for all entities
- **Easy Export/Import** – Simple data portability
- **Version Control Friendly** – Text-based format

---

## 🏗 System Architecture

```
┌───────────────────────────────────────────┐
│         CLI Menu Interface                │
└──────────────┬────────────────────────────┘
               │
               ▼
┌───────────────────────────────────────────┐
│      Student Manager Module               │
│  ┌────────────┐  ┌──────────────────┐    │
│  │ Add/View   │  │ Update Records   │    │
│  └────────────┘  └──────────────────┘    │
└──────────────┬────────────────────────────┘
               │
               ▼
┌───────────────────────────────────────────┐
│      Course Manager Module                │
│  ┌────────────┐  ┌──────────────────┐    │
│  │ Add Course │  │ Student Mapping  │    │
│  └────────────┘  └──────────────────┘    │
└──────────────┬────────────────────────────┘
               │
               ▼
┌───────────────────────────────────────────┐
│      Faculty Manager Module               │
│  ┌────────────┐  ┌──────────────────┐    │
│  │ Add Faculty│  │ Course Mapping   │    │
│  └────────────┘  └──────────────────┘    │
└──────────────┬────────────────────────────┘
               │
               ▼
┌───────────────────────────────────────────┐
│      Marks Manager Module                 │
│  ┌────────────┐  ┌──────────────────┐    │
│  │ Add Marks  │  │ View Performance │    │
│  └────────────┘  └──────────────────┘    │
└──────────────┬────────────────────────────┘
               │
               ▼
┌───────────────────────────────────────────┐
│      Test Scheduler Module                │
│  ┌────────────┐  ┌──────────────────┐    │
│  │ Schedule   │  │ View Calendar    │    │
│  └────────────┘  └──────────────────┘    │
└──────────────┬────────────────────────────┘
               │
               ▼
┌───────────────────────────────────────────┐
│      Task Manager Module                  │
│  ┌────────────┐  ┌──────────────────┐    │
│  │ Add Tasks  │  │ Track Status     │    │
│  └────────────┘  └──────────────────┘    │
└──────────────┬────────────────────────────┘
               │
               ▼
┌───────────────────────────────────────────┐
│    CSV Storage Layer (7 Data Files)      │
└───────────────────────────────────────────┘
```

Everything interacts through **CSV data pipelines**, making the system lightweight, fast, and portable.

---

## 📦 Installation

### Prerequisites
- Python 3.6 or higher
- No external dependencies required
- Works on Windows, macOS, and Linux

### Setup Steps

1. **Extract the project**
```bash
unzip Student_Management_System-main.zip
cd Student_Management_System-main
```

2. **Verify Python installation**
```bash
python --version
# or
python3 --version
```

3. **Check CSV files** (should be present)
```bash
ls *.csv
```

4. **Run the system**
```bash
python F13CPSlabeval3.py
# or
python3 F13CPSlabeval3.py
```

**No external libraries required** – Pure Python + CSV!

---

## 🚀 Usage

### Running the System

**Start the CLI interface:**
```bash
python F13CPSlabeval3.py
```

**Follow the interactive menu** to perform operations.

**Example Workflow:**
```
1. Add Student → Enter details → Data saved to student_info.csv
2. Add Course → Enter course info → Saved to course_info.csv
3. Add Faculty → Register instructor → Stored in faculty_info.csv
4. Map Faculty to Course → Create teaching assignments
5. Add Marks → Record grades for students
6. Schedule Test → Plan upcoming exams
```

### CLI Menu Options

```
═══════════════════════════════════════════
    STUDENT MANAGEMENT SYSTEM
═══════════════════════════════════════════
1.  Add Student
2.  View Students
3.  Add Course
4.  View Courses
5.  Add Faculty
6.  View Faculty
7.  Map Faculty to Course
8.  View Faculty-Course Mappings
9.  Add Marks
10. View Marks
11. Add Task
12. View Tasks
13. Schedule Test
14. View Test Schedule
15. Exit
═══════════════════════════════════════════
Enter your choice: 
```

---

## 📁 Project Structure

```
Student_Management_System-main/
│
├── F13CPSlabeval3.py        # Main executable
│
├── student_info.csv         # Student records
├── course_info.csv          # Course list
├── faculty_info.csv         # Faculty data
├── student_marks.csv        # Marks data
├── faculty_course_info.csv  # Teaching assignments
├── tasks.csv                # Student tasks
├── test_schedule.csv        # Exam schedules
│
└── README.md                # Documentation
```

### CSV File Schemas

#### **student_info.csv**
```csv
student_id,name,branch,year
1,Sharvesh,CSE,1
2,Akhil,EEE,2
3,Priya,MECH,3
```

| Column | Type | Description |
|--------|------|-------------|
| student_id | Integer | Unique student identifier |
| name | String | Student full name |
| branch | String | Department/Branch code |
| year | Integer | Current academic year |

#### **course_info.csv**
```csv
course_id,course_name,credits
CS101,Python Programming,4
CS102,Data Structures,3
EE201,Circuit Theory,4
```

| Column | Type | Description |
|--------|------|-------------|
| course_id | String | Unique course code |
| course_name | String | Full course name |
| credits | Integer | Credit hours |

#### **faculty_info.csv**
```csv
faculty_id,name,department
FC01,Dr. Kumar,CSE
FC02,Dr. Sharma,EEE
FC03,Prof. Singh,MECH
```

| Column | Type | Description |
|--------|------|-------------|
| faculty_id | String | Unique faculty identifier |
| name | String | Faculty full name |
| department | String | Department code |

#### **student_marks.csv**
```csv
student_id,course_id,marks
1,CS101,95
1,CS102,88
2,EE201,92
```

| Column | Type | Description |
|--------|------|-------------|
| student_id | Integer | Student reference |
| course_id | String | Course reference |
| marks | Integer | Grade (0-100) |

#### **faculty_course_info.csv**
```csv
faculty_id,course_id
FC01,CS101
FC01,CS102
FC02,EE201
```

| Column | Type | Description |
|--------|------|-------------|
| faculty_id | String | Faculty reference |
| course_id | String | Course reference |

#### **tasks.csv**
```csv
student_id,task,deadline,status
1,Submit Assignment 1,2025-01-25,Pending
1,Complete Lab Report,2025-01-28,Complete
2,Project Presentation,2025-02-05,Pending
```

| Column | Type | Description |
|--------|------|-------------|
| student_id | Integer | Student reference |
| task | String | Task description |
| deadline | Date | Due date (YYYY-MM-DD) |
| status | String | Pending/Complete |

#### **test_schedule.csv**
```csv
date,time,course_id,faculty_id
2025-01-29,10:00,CS101,FC01
2025-02-05,14:00,CS102,FC01
2025-02-10,09:00,EE201,FC02
```

| Column | Type | Description |
|--------|------|-------------|
| date | Date | Test date (YYYY-MM-DD) |
| time | Time | Test time (HH:MM) |
| course_id | String | Course reference |
| faculty_id | String | Invigilator reference |

---

## 🔍 Core Modules

### 1. Student Manager
**Functions:**
- `add_student()` – Register new student with auto-generated ID
- `view_students()` – Display all students in tabular format
- `update_student()` – Modify existing student records
- `search_student(student_id)` – Find student by ID

**Data Flow:**
```
User Input → Validation → student_info.csv → Confirmation
```

### 2. Course Manager
**Functions:**
- `add_course()` – Create new course with ID, name, credits
- `view_courses()` – List all available courses
- `delete_course()` – Remove course (with cascade checks)
- `enroll_student()` – Map students to courses

**Business Logic:**
- Prevents duplicate course IDs
- Validates credit hours (1-6)
- Checks prerequisites before enrollment

### 3. Faculty Manager
**Functions:**
- `add_faculty()` – Register faculty with department
- `view_faculty()` – Display faculty directory
- `assign_course()` – Map faculty to teaching courses
- `view_teaching_load()` – Show courses per faculty

**Constraints:**
- One faculty can teach multiple courses
- One course can have only one faculty

### 4. Marks Manager
**Functions:**
- `add_marks()` – Record grades (0-100)
- `update_marks()` – Modify existing grades
- `view_marks(student_id)` – Student grade report
- `calculate_gpa()` – Compute GPA from marks

**Validation:**
- Marks must be 0-100
- Student must be enrolled in course
- Prevents duplicate entries

### 5. Test Scheduler
**Functions:**
- `schedule_test()` – Create exam with date, time, course
- `view_schedule()` – Display upcoming tests
- `check_conflict()` – Prevent overlapping exams
- `reschedule_test()` – Modify existing schedule

**Features:**
- Conflict detection (same date/time/faculty)
- Calendar view
- Faculty availability check

### 6. Task Manager
**Functions:**
- `add_task()` – Create task with deadline
- `view_tasks(student_id)` – Personal task list
- `update_status()` – Mark complete/pending
- `view_pending()` – Show overdue tasks

**Tracking:**
- Deadline monitoring
- Status updates
- Per-student task lists

---

## 📊 Data Flow Overview

```
                    ┌──────────────┐
                    │   User CLI   │
                    └───────┬──────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
        ▼                   ▼                   ▼
┌───────────────┐   ┌──────────────┐   ┌──────────────┐
│   Validation  │   │  Processing  │   │   Display    │
│    Layer      │   │    Layer     │   │    Layer     │
└───────┬───────┘   └──────┬───────┘   └──────┬───────┘
        │                   │                   │
        └───────────────────┼───────────────────┘
                            │
                    ┌───────▼──────┐
                    │  CSV Storage │
                    └──────────────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
        ▼                   ▼                   ▼
┌──────────────┐   ┌──────────────┐   ┌──────────────┐
│ student_     │   │  course_     │   │ faculty_     │
│ info.csv     │   │  info.csv    │   │ info.csv     │
└──────────────┘   └──────────────┘   └──────────────┘
        │                   │                   │
        ▼                   ▼                   ▼
┌──────────────┐   ┌──────────────┐   ┌──────────────┐
│ student_     │   │ faculty_     │   │ test_        │
│ marks.csv    │   │ course_      │   │ schedule.csv │
│              │   │ info.csv     │   │              │
└──────────────┘   └──────────────┘   └──────────────┘
                            │
                            ▼
                    ┌──────────────┐
                    │  tasks.csv   │
                    └──────────────┘
```

---

## ⚙️ Configuration

### System Settings

Create a `config.py` file for custom settings:

```python
# File paths
CSV_DIRECTORY = './'
BACKUP_DIRECTORY = './backups/'

# Display settings
TABLE_WIDTH = 80
RESULTS_PER_PAGE = 20

# Validation rules
MIN_MARKS = 0
MAX_MARKS = 100
MIN_CREDITS = 1
MAX_CREDITS = 6

# ID generation
STUDENT_ID_PREFIX = 'STU'
FACULTY_ID_PREFIX = 'FAC'
COURSE_ID_PREFIX = 'CRS'

# Date format
DATE_FORMAT = '%Y-%m-%d'
TIME_FORMAT = '%H:%M'
```

### Customization Options

**Modify CSV paths in main script:**
```python
STUDENT_FILE = 'student_info.csv'
COURSE_FILE = 'course_info.csv'
FACULTY_FILE = 'faculty_info.csv'
# ... etc
```

**Enable logging:**
```python
import logging

logging.basicConfig(
    filename='sms.log',
    level=logging.INFO,
    format='%(asctime)s - %(levelname)s - %(message)s'
)
```

---

## 🛠 Development

### Adding New Features

**Example: Add Student Search by Name**
```python
def search_student_by_name(name):
    with open('student_info.csv', 'r') as file:
        reader = csv.DictReader(file)
        for row in reader:
            if name.lower() in row['name'].lower():
                print(f"ID: {row['student_id']}, Name: {row['name']}")
```

**Example: Calculate Class Average**
```python
def calculate_class_average(course_id):
    total = 0
    count = 0
    with open('student_marks.csv', 'r') as file:
        reader = csv.DictReader(file)
        for row in reader:
            if row['course_id'] == course_id:
                total += int(row['marks'])
                count += 1
    return total / count if count > 0 else 0
```

### Extending Modules

**Add GPA Calculation:**
```python
GRADE_SCALE = {
    'A+': 10, 'A': 9, 'B+': 8, 'B': 7,
    'C+': 6, 'C': 5, 'D': 4, 'F': 0
}

def calculate_gpa(student_id):
    # Implementation here
    pass
```

---

## 🧪 Testing

### Manual Testing Checklist

- [ ] Add student with valid data
- [ ] Add student with duplicate ID (should fail)
- [ ] View all students
- [ ] Add course
- [ ] Map faculty to course
- [ ] Add marks (valid range)
- [ ] Add marks (invalid range - should fail)
- [ ] Schedule test
- [ ] Schedule conflicting test (should fail)
- [ ] Add task with deadline
- [ ] View complete system data

### Data Validation Tests

```python
# Test marks validation
assert 0 <= marks <= 100, "Invalid marks range"

# Test date format
from datetime import datetime
try:
    datetime.strptime(date_str, '%Y-%m-%d')
except ValueError:
    print("Invalid date format")

# Test duplicate prevention
if student_id in existing_ids:
    print("Student ID already exists")
```

---

## 🔧 Troubleshooting

### Common Issues

**Issue:** `FileNotFoundError: student_info.csv`
```bash
# Solution: Create CSV files with headers
touch student_info.csv
echo "student_id,name,branch,year" > student_info.csv
```

**Issue:** CSV data corruption or misaligned columns
```bash
# Solution: Validate CSV structure
python -c "import csv; csv.Sniffer().sniff(open('student_info.csv').read(1024))"
```

**Issue:** Permission denied when writing to CSV
```bash
# Solution: Check file permissions
chmod 644 *.csv
```

**Issue:** Special characters breaking CSV format
```python
# Solution: Use proper escaping
import csv
with open('file.csv', 'w', newline='', encoding='utf-8') as f:
    writer = csv.writer(f, quoting=csv.QUOTE_MINIMAL)
```

### Data Recovery

**Backup CSV files regularly:**
```bash
# Create backup script
cp *.csv backups/backup_$(date +%Y%m%d).csv
```

**Restore from backup:**
```bash
cp backups/backup_20250120.csv student_info.csv
```

---

## 🚧 Roadmap

### Phase 1: Core Enhancements
- [ ] Input validation for all fields
- [ ] Error handling and logging
- [ ] Data backup automation
- [ ] Search and filter functionality
- [ ] Bulk import/export via CSV

### Phase 2: Database Migration
- [ ] Convert CSV to SQLite database
- [ ] Implement proper relationships (foreign keys)
- [ ] Add transaction support
- [ ] Create database schema migration scripts
- [ ] Query optimization

### Phase 3: User Interface
- [ ] Build GUI using Tkinter/PyQt
- [ ] Web interface with Flask/Django
- [ ] Dashboard with statistics
- [ ] Report generation (PDF/Excel)
- [ ] Data visualization charts

### Phase 4: Advanced Features
- [ ] User authentication (admin/faculty/student roles)
- [ ] Email notifications for deadlines
- [ ] Attendance tracking module
- [ ] Fee management system
- [ ] Library management integration
- [ ] Mobile app (React Native/Flutter)

### Phase 5: Cloud & Deployment
- [ ] REST API development
- [ ] Cloud storage integration (AWS S3, Google Drive)
- [ ] Multi-tenant architecture
- [ ] Docker containerization
- [ ] CI/CD pipeline
- [ ] Load testing and performance optimization

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

### How to Contribute

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Make your changes**
4. **Test thoroughly**
5. **Commit with descriptive messages**
   ```bash
   git commit -m "Add student GPA calculation feature"
   ```
6. **Push to your fork**
   ```bash
   git push origin feature/AmazingFeature
   ```
7. **Open a Pull Request**

### Coding Standards

- Follow PEP 8 style guide
- Add docstrings to all functions
```python
def add_student(name, branch, year):
    """
    Add a new student to the system.
    
    Args:
        name (str): Student full name
        branch (str): Department code
        year (int): Current academic year
    
    Returns:
        int: Generated student ID
    """
    pass
```
- Include error handling
- Write unit tests for new features
- Update README with new functionality
- Keep CSV structure consistent

### Areas for Contribution

- 🐛 Bug fixes
- ✨ New features
- 📝 Documentation improvements
- 🎨 UI/UX enhancements
- 🧪 Test coverage
- 🌐 Internationalization
- ♿ Accessibility features

---

## 📄 License

This project is free to use for **educational and personal development purposes**.

### Usage Terms
- ✅ Use in academic projects
- ✅ Modify and extend
- ✅ Share with others
- ✅ Use as learning resource
- ⚠️ No warranty provided
- ⚠️ Use at your own risk

For commercial use, please contact the maintainers.

---

## 🙏 Acknowledgements

- **Python CSV Module** – Built-in library for CSV handling
- **Academic Institutions** – Real-world requirements inspiration
- **Open Source Community** – Best practices and design patterns
- **Contributors** – Everyone who improves this project

### Educational Resources
- Python Documentation: https://docs.python.org/3/library/csv.html
- CSV File Format Specification
- Database Design Principles
- Software Engineering Best Practices

---

## 📧 Contact & Support

- **Issues:** Report bugs via GitHub Issues
- **Discussions:** Join our community forum
- **Email:** support@studentmanagementsystem.com
- **Documentation:** Full docs available in `/docs` directory

### Quick Links
- [Installation Guide](#installation)
- [Usage Examples](#usage)
- [API Documentation](#core-modules)
- [Contribution Guidelines](#contributing)
- [Troubleshooting](#troubleshooting)

---

## 📈 Project Statistics

- **Language:** Python 3
- **Lines of Code:** ~1,500
- **Modules:** 6 core modules
- **CSV Files:** 7 data files
- **Development Status:** Active
- **License:** Educational Use

---

**Made with ❤️ for Academic Institutions**

*Simplifying student data management, one CSV at a time.*
