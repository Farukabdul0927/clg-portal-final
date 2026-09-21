COLLEGE PORTAL - UPDATED

ACADEMIC ROLL-NUMBER FORMAT
---------------------------
Y24  = 3rd Year regular students (CSE / ECE)
L25  = 3rd Year lateral students (CSE / ECE)
Y25  = 2nd Year regular students (CSE / AIML currently supplied; ECE pending)
L26  = 2nd Year lateral students (CSE / AIML currently supplied; ECE pending)

2ND YEAR DATA INCLUDED
----------------------
CSE regular: Y25CSE279001 - Y25CSE279066 (CSE-A)
CSE lateral: L26CSE279001 - L26CSE279009 (CSE-A), L26CSE279010 - L26CSE279014 (CSE-B)
AIML regular: Y25AIML279001 - Y25AIML279042
AIML lateral: L26AIML279001 - L26AIML279018

3RD YEAR DATA
-------------
Existing Y24 and L25 CSE/ECE data is retained. Y24 accounts are normalized to 3rd Year.

AIML USERNAMES / PASSWORDS
--------------------------
AIML usernames use the student's name portion (not the first surname/initial token) with a roll-number suffix when needed for uniqueness.
Passwords are the last six digits of the roll number, e.g. 279001.

LOGIN
-----
The Student and Teacher login pages now ask for:
1. Year
2. Group / Section
3. Username
4. Password

The selected student year and group are validated against the account.
Teacher login stores the selected year and group so teacher attendance/marks student lists are limited to that selection.

PORTAL FEATURES RETAINED
------------------------
Student: Dashboard, Attendance, Timetable, Marks, Results, Notices, Assignments, Study Materials, Chat, Profile, Account.
Teacher: Dashboard, Attendance, Timetable, Marks, Results, Notices, Assignments, Study Materials/PDFs, Chat, Account.
Admin: Dashboard, Students, Teachers, Chat, Notifications.

CHAT
----
Each Year + Group has two boards:
- Students Only
- Students + Teachers

The + button beside the message box supports file attachments. Links can be typed directly. Uploaded chat files are stored in static/chat_files.

NOTIFICATIONS
-------------
Portal updates create notifications/events. Student, teacher and admin portals poll for new events and play a short notification sound. Events are filtered by year and group for students/teachers; admin receives all events.

ADMIN LOGIN
-----------
Username: faruk
Password: admin

RUN
---
Open a terminal in the inner "clg portal" folder and run:
python app.py
Then open http://127.0.0.1:5000/
