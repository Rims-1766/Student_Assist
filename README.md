# StudentAssist AI Portal

StudentAssist is a responsive college helpdesk prototype built with plain HTML, CSS, and JavaScript. It provides role-based login, a student dashboard with an AI-style query assistant, and an admin dashboard for managing college records such as notices, events, exams, materials, and student details.

## Highlights

- Role-based demo login for students and administrators
- Student dashboard with profile details, academic metrics, notices, events, exams, and study materials
- Rule-based chatbot for common college queries such as timetable, fees, exams, placements, facilities, notices, and materials
- Chat history saved in the browser with quick replay and clear-history support
- Admin dashboard for adding, editing, deleting, and previewing records
- Persistent demo data using `localStorage`
- Responsive layouts for desktop, tablet, and mobile screens
- No framework, build tool, package manager, or server required

## Demo Credentials

Use any of the following accounts from the login page:

| Role | Email | Password |
| --- | --- | --- |
| Admin | `admin@college.com` | `admin123` |
| Admin | `admin@college.edu` | `admin123` |
| Student | `student1@college.com` | `student123` |
| Student | `student2@college.com` | `student456` |
| Student | `student3@college.com` | `student789` |
| Student | `student@college.edu` | `student123` |

## Project Structure

```text
Student_Asist/
├── Login.html
├── student.html
├── student-dashboard.css
├── admin.html
├── admin-dashboard.css
├── studentassist-login-hero.png
└── README.md
```

## Getting Started

Because this is a static frontend project, you can run it directly in a browser.

1. Download or clone the project.
2. Open `Login.html` in your browser.
3. Sign in with one of the demo accounts.
4. The app redirects you to the correct dashboard based on the selected role.

For the cleanest local preview, you can also serve the folder with any static server:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/Login.html
```

## Pages

### Login

`Login.html` contains the role-based sign-in screen. It validates demo credentials in the browser and redirects users to either `student.html` or `admin.html`.

### Student Dashboard

`student.html` gives students a central academic portal with:

- Student profile information
- Academic summary cards
- AI-style chatbot with quick actions
- Saved chat history
- Latest notices
- Upcoming events
- Exam schedule
- Study materials

### Admin Dashboard

`admin.html` gives administrators tools to manage portal data with:

- Dashboard metrics
- Domain selector for notices, events, exams, materials, and students
- Add-record and update-record form
- Editable record table
- Delete confirmation
- Student-facing preview cards

## Data Storage

The project uses browser `localStorage` for demo persistence.

| Key | Purpose |
| --- | --- |
| `userRole` | Stores the current logged-in role |
| `userEmail` | Stores the logged-in admin email |
| `studentEmail` | Stores the logged-in student email |
| `studentChatHistory` | Stores recent student chatbot questions and answers |
| `studentAssistAdminData` | Stores admin-managed records |

To reset all demo data, clear the browser's site data or run this in the browser console:

```js
localStorage.clear();
```

## Customization

- Update demo users in the `adminUsers` and `studentUsers` arrays inside `Login.html`.
- Update chatbot responses in the `replies` array inside `student.html`.
- Update starter admin records in the `starterData` object inside `admin.html`.
- Adjust the student dashboard design in `student-dashboard.css`.
- Adjust the admin dashboard design in `admin-dashboard.css`.
- Replace `studentassist-login-hero.png` to change the login page artwork.

## Notes

This project is a frontend prototype. Authentication, authorization, database storage, and chatbot intelligence are simulated in the browser for demonstration purposes. For production use, connect the app to a secure backend, move credentials out of the frontend, validate user sessions on the server, and store records in a real database.

## Tech Stack

- HTML5
- CSS3
- Vanilla JavaScript
- Browser `localStorage`

## License

This project is available for learning, portfolio, and prototype use. Add a formal license file if you plan to publish or distribute it.
