
# Career Guidance - Online Quiz Platform

An **Online Quiz** system for students, teachers, and administrators, designed to manage and conduct exams efficiently.

## Features

### **Admin**
- Create an Admin account using the command:
  ```bash
  py manage.py createsuperuser
  ```
- After login, the Admin can:
  - View the **Dashboard** with total counts of students, teachers, courses, and questions.
  - **Manage Teachers**: View, update, delete, and approve teacher accounts.
  - **Manage Students**: View, update, and delete student accounts.
  - View student exam results and marks.
  - **Manage Courses/Exams**: Add, view, and delete courses/exams.
  - **Manage Questions**: Add questions to courses with options, correct answers, and marks. Also, view and delete questions.

### **Teacher**
- Apply for a job in the system. Admin approval is required to log in.
- After login, the Teacher can:
  - View the **Dashboard** with total counts of students, courses, and questions.
  - **Manage Courses/Exams**: Add, view, and delete courses/exams.
  - **Manage Questions**: Add questions to courses with options, correct answers, and marks. Also, view and delete questions.

  **Note**: Admins hire teachers to manage courses and questions.

### **Student**
- Create an account (no approval needed by Admin).
- After login, the Student can:
  - View the **Dashboard** with total courses/exams and questions available.
  - Take exams without any limit on the number of attempts.
  - View marks for each exam attempt.

### **Exam Features**
- Question pattern is **MCQ** (Multiple Choice Questions) with 4 options and 1 correct answer.

---

## How to Run This Project

1. **Install Python** (Version 3.7.6 recommended).
   - **Important**: Don’t forget to tick "Add to Path" while installing Python.
   
2. **Install dependencies** by running the following command in the terminal:
   ```bash
   python -m pip install -r requirements.txt
   ```

3. **Download** the project ZIP folder and extract it.

4. Navigate to the project folder in the terminal and run the following commands:

   ```bash
   py manage.py makemigrations
   py manage.py migrate
   py manage.py runserver
   ```

5. Open your browser and enter the following URL to access the project:
   ```
   http://127.0.0.1:8000/
   ```

---

## Contact Us Page Configuration

In the `settings.py` file, update the following configurations with your email credentials:

```python
EMAIL_HOST_USER = 'youremail@gmail.com'
EMAIL_HOST_PASSWORD = 'your email password'
EMAIL_RECEIVING_USER = 'youremail@gmail.com'
```

---

## Screenshots

### Homepage
![Homepage Snapshot](link-to-homepage-screenshot)

### Admin Dashboard
![Dashboard Snapshot](link-to-dashboard-screenshot)

### Exam Rules
![Rules Snapshot](link-to-rules-screenshot)

### Exam Page
![Exam Snapshot](link-to-exam-screenshot)

### Teacher Panel
![Teacher Panel Snapshot](link-to-teacher-panel-screenshot)

---

## Known Issues & Limitations
- **Admin/Teacher Question Management**: Admins and teachers can add an unlimited number of questions to any course. However, when creating a course, the admin specifies a fixed number of questions, which could lead to inconsistencies in exams if not properly managed.
