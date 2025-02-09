# Work Time Calculator

## **Overview**
The **Work Time Calculator** is a web application designed to help users track the time they spend on various tasks, goals, or activities. It allows users to create goals, start/stop timers, view progress analytics, and develop consistent work habits with gamified features like streaks and badges.

---

## **Tech Stack**

### **Frontend**
- **React.js**: For building the user interface and ensuring a dynamic user experience.
- **Libraries**:
  - Axios: For API communication.
  - Tailwind CSS: For responsive and modern styling.

### **Backend**
- **Django**: For creating RESTful APIs, managing business logic, and handling server-side operations.
- **Django Rest Framework (DRF)**: For building robust and scalable APIs.

### **Database**
- **MySQL**: For structured and relational data management.

### **Other Tools**
- **Postman**: For testing APIs.
- **Chart.js / Recharts**: For visualizing analytics and reports.
- **Heroku/AWS**: For backend deployment.
- **Netlify/Vercel**: For frontend deployment.

---

## **Features**

### **Phase 1: Core Features (MVP)**
1. **User Authentication**
   - Secure signup/login.
   - Option for social login (Google, GitHub).

2. **Goal Management**
   - Create, view, update, and delete goals.
   - Assign priorities to goals (High, Medium, Low).

3. **Timer Functionality**
   - Start/stop timers manually for any goal.
   - Automatically calculate and log session duration.

4. **Time Logs**
   - Maintain session data with start time, end time, and duration.
   - Display logs in a simple table.

5. **Basic Dashboard**
   - View total time spent on each goal.
   - Display recent logs.

### **Phase 2: Usability Enhancements**
6. **Progress Insights**
   - Show daily/weekly/monthly time distribution.
   - Display trends over time.

7. **Calendar View**
   - Visualize daily work logs using a calendar.

8. **Notifications & Reminders**
   - Set custom reminders for specific goals.
   - Notify users when daily goals are achieved.

### **Phase 3: Advanced Features**
9. **Gamification**
   - Add streaks, badges, and achievements for milestones.

10. **Pomodoro Timer Mode**
    - Introduce focus intervals (e.g., 25 minutes work, 5 minutes break).

11. **Analytics**
    - Advanced visualizations for time distribution.
    - Weekly and monthly performance insights.

12. **AI Recommendations**
    - Suggest best work hours based on user patterns.
    - Recommend goals to prioritize.

---

## **Setup Instructions**

### **Frontend Setup**
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/work-time-calculator.git
   cd work-time-calculator/frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm start
   ```
4. Access the app at `http://localhost:3000`.

### **Backend Setup**
1. Navigate to the backend folder:
   ```bash
   cd ../backend
   ```
2. Set up a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate # For Linux/Mac
   venv\Scripts\activate # For Windows
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Set up the database:
   - Install and configure MySQL.
   - Create a database (e.g., `work_time_calculator`).
   - Update `settings.py` with database credentials:
     ```python
     DATABASES = {
         'default': {
             'ENGINE': 'django.db.backends.mysql',
             'NAME': 'work_time_calculator',
             'USER': 'your_mysql_user',
             'PASSWORD': 'your_mysql_password',
             'HOST': 'localhost',
             'PORT': '3306',
         }
     }
     ```
5. Apply migrations:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```
6. Start the development server:
   ```bash
   python manage.py runserver
   ```

---

## **Usage**
1. Open the application in your browser.
2. Sign up and create a new account.
3. Add your goals (e.g., "Learn Python").
4. Start the timer for a goal and track your work.
5. View logs and analyze your progress in the dashboard.

---

## **Database Schema**

### **Users Table**
| Field       | Type        | Description           |
|-------------|-------------|-----------------------|
| UserID      | INT (PK)    | Unique user ID.       |
| Name        | VARCHAR(100)| User's name.          |
| Email       | VARCHAR(100)| User's email address. |
| PasswordHash| VARCHAR(255)| Hashed password.      |

### **Goals Table**
| Field       | Type          | Description                 |
|-------------|---------------|-----------------------------|
| GoalID      | INT (PK)      | Unique goal ID.             |
| UserID      | INT (FK)      | Associated user ID.         |
| GoalName    | VARCHAR(255)  | Name of the goal.           |
| Priority    | ENUM          | Goal priority (High/Medium/Low). |
| TotalTime   | INT           | Total time spent (minutes). |

### **TimeLogs Table**
| Field       | Type          | Description                 |
|-------------|---------------|-----------------------------|
| LogID       | INT (PK)      | Unique log ID.              |
| UserID      | INT (FK)      | Associated user ID.         |
| GoalID      | INT (FK)      | Associated goal ID.         |
| StartTime   | DATETIME      | Start time of the session.  |
| EndTime     | DATETIME      | End time of the session.    |
| Duration    | INT           | Duration in minutes.        |

---

## **Future Enhancements**
- Add team collaboration features.
- Implement offline support for the timer.
- Export data to PDF/CSV.
- Mobile app development (React Native/Flutter).

---

## **Contributing**
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit changes:
   ```bash
   git commit -m "Add feature description"
   ```
4. Push to your branch:
   ```bash
   git push origin feature-name
   ```
5. Create a pull request.

---

## **License**
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## **Contact**
For questions or feedback, feel free to reach out:
- **Email**: kaustubhpy@gmail.com
- **GitHub**: [149189](https://github.com/149189)
- **LinkedIn**: [Kaustubh Ratwadkar]([https://linkedin.com/in/your-linkedin-profile](https://www.linkedin.com/in/kaustubh-ratwadkar-20699a223/))
- **Phone**: +91 8657092872
---

Happy Coding! 🚀
