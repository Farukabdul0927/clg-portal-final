# College Portal - Hosting Ready

This copy is prepared for deployment on Render.

## Local
```bash
pip install -r requirements.txt
python app.py
```

## Render
1. Upload/push the contents of this folder to a GitHub repository.
2. In Render, create a **New Web Service** and select that GitHub repository.
3. Render can use `render.yaml`, or set:
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `gunicorn app:app`
4. Deploy. Render will give you a public `onrender.com` URL.

Admin login:
- Username: `faruk`
- Password: `admin`

## Important database note
The project currently uses SQLite. This is fine for a demonstration, but Render's normal web-service filesystem is not persistent, so data added after deployment can be lost when the service is redeployed/restarted. For a production portal, move the database to PostgreSQL (or attach persistent storage where supported).

The bundled `instance/database.db` is retained in this hosting-ready copy so the current local data can be used if you commit that file to GitHub. The `.gitignore` has been adjusted so the database is not silently ignored.

NEW FEATURES
- Student and teacher login can use username/password or registered phone/password.
- Remember me keeps a successful login for 30 days.
- Forgot Username and Forgot Password use registered phone + OTP.
- Real SMS OTP requires Twilio Verify environment variables on Render:
  TWILIO_ACCOUNT_SID
  TWILIO_AUTH_TOKEN
  TWILIO_VERIFY_SERVICE_SID
- Register each user's phone number from Student/Teacher Account Settings or Admin management when creating an account.
- A separate Private Chat page lets users enter a student roll number for a one-to-one chat.
- Student timetable now always loads a group timetable/default schedule instead of returning "Timetable is not available."

## New login and phone features
- Students and teachers can sign in with username/password or registered phone/password.
- Forgot Username and Forgot Password use the registered phone and OTP.
- Admin can also sign in with username/password or registered admin phone/password.
- Admin can register/update the admin phone from the Admin Dashboard.
- Admin Students and Teachers pages display each registered phone number; accounts without a phone show "Not registered".
- To enable real SMS OTP on Render, set TWILIO_ACCOUNT_SID, TWILIO_AUTH_TOKEN, and TWILIO_VERIFY_SERVICE_SID environment variables.
