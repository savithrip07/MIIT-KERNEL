> **Note:** This repository is a personal fork of the original MIIT-KERNEL project. The following section highlights my individual contributions to the project.

## My Contribution

As part of the MIIT-KERNEL development team, I contributed to the early development and frontend implementation of the platform.

### Responsibilities

- Established the initial frontend structure and layouts for key application pages
- Developed the foundational UI components and application workflow that were later expanded and refined by the team
- Contributed to the initial backend setup and integration during the early stages of development
- Connected frontend interfaces with backend data and application functionality
- Implemented and supported music/audio-related features within the platform
- Assisted in feature development, user interface improvements, and overall user experience design
- Collaborated with team members on integrating and refining platform features

### Areas Contributed

- Frontend development and UI foundations
- Page structure and application flow
- Early-stage backend integration
- Music/audio-related functionality
- Feature integration and user experience enhancements

---

# MIIT-KERNEL — Learning Companion Platform

A full-stack study management web app built with Flask, featuring role-based dashboards, TA matching, live speech-to-notes, study timers, and AI-generated timetables.

---

## Features

### Students
- 10 study timer modes (Pomodoro, Deep Focus, 52-17, Flowtime, etc.)
- Swipe-based TA matching system
- Live speech-to-notes transcription
- AI-generated timetable from deadlines
- Study stats and focus tracking

### Teaching Assistants
- Accept/decline student match requests
- Upload and share notes
- Conduct live sessions

### Admins
- User management and role control
- Platform-wide analytics and match monitoring

---

## Tech Stack

| Layer     | Technology                        |
|-----------|-----------------------------------|
| Backend   | Flask, Flask-SocketIO, SQLAlchemy |
| Database  | SQLite                            |
| Frontend  | HTML, Bootstrap 5, Chart.js       |
| Speech    | Deepgram SDK / Web Speech API     |

---

## Project Structure

```
MIIT-KERNEL/
├── app.py                        # Main Flask app and routes
├── requirements.txt              # Python dependencies
├── auth/
│   └── utils.py                  # Auth helpers (hashing, decorators)
├── database/
│   ├── db.py                     # SQLAlchemy models
│   └── schema.sql                # Raw schema
├── services/
│   ├── ai_matching_service.py    # TA-student matching logic
│   ├── real_speech_service.py    # Live transcription service
│   └── transcription_service.py
├── templates/
│   ├── student/                  # Student-facing pages
│   ├── ta/                       # TA-facing pages
│   ├── admin/                    # Admin pages
│   ├── landing.html
│   ├── login.html
│   └── base.html
└── static/
    └── css/styles.css
```

---

## Setup

1. **Clone the repo**
   ```bash
   git clone https://github.com/smritis21/MIIT-KERNEL.git
   cd MIIT-KERNEL
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the app**
   ```bash
   python app.py
   ```

4. **Open in browser**
   ```
   http://localhost:5000
   ```

The SQLite database is created automatically on first run.

---

## Roles

| Role    | Access                                          |
|---------|-------------------------------------------------|
| Student | Timers, TA matching, notes, timetable, stats    |
| TA      | Student management, notes upload, live sessions |
| Admin   | User management, platform analytics             |

Create accounts via the signup page and select the appropriate role.

---

## Seeding & Utilities

```bash
python seed_database.py        # Seed sample data
python create_tas.py           # Create TA accounts
python migrate_and_seed.py     # Run migrations + seed
```
