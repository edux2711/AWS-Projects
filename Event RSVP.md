# Event RSVP – AWS Full-Stack Web Application

A simple AWS-powered app that lists events, shows details & stats, and accepts RSVPs.  

---

## 🧱 Architecture Overview

**Frontend → API Gateway → Lambda → MySQL + DynamoDB → S3 + CloudFront**
<img width="946" height="460" alt="Screenshot 2026-04-14 at 5 29 29 PM" src="https://github.com/user-attachments/assets/ad19057b-2664-435b-bfc4-bda00458f89c" />

---

<img width="1313" height="927" alt="Screenshot 2026-04-14 at 5 03 37 PM" src="https://github.com/user-attachments/assets/394d3ef6-5e88-4755-b34c-27ded3952e66" />
<img width="1313" height="694" alt="Screenshot 2026-04-14 at 5 03 10 PM" src="https://github.com/user-attachments/assets/f9d11921-2e5e-4b29-8e7f-cbcdaf3f6a13" />

---



## 📁 Project Structure

```
.
├── index.html           # Main UI
├── style.css            # Styling
├── app.js               # Entry script (loads events)
├── events.js            # Event logic + modal + RSVP
├── utils.js             # API helpers & formatters
├── index.js             # Lambda backend handler
├── database-notes.txt   # SQL Commands
├── package.json
├── package-lock.json
└── .gitignore
```

**.gitignore**
```
node_modules/
.DS_Store
```

---

### Backend (Lambda)

Set these **environment variables** in your Lambda configuration. Feel free to customize:

| Variable | Example | Description |
|-----------|----------|-------------|
| REGION  | ap-southeast-1 | AWS region |
| DB_HOST | mydb.xxxxx.ap-southeast-1.rds.amazonaws.com | MySQL host |
| DB_USER | admin | MySQL user |
| DB_PASS | ******** | MySQL password |
| DB_NAME | eventsdb | MySQL database |

**Install dependencies**
```bash
npm install
```

---

### API Summary

| Method | Path | Purpose |
|---------|------|----------|
| GET | `/events` | Fetch all events |
| GET | `/event/{event_id}` | Fetch single event |
| GET | `/stats/{event_id}` | Get RSVP counts |
| GET | `/attendees/{event_id}` | Get attendee list |
| POST | `/rsvp` | Submit RSVP |

Make sure **CORS** is set up properly.

---

### Hosting (S3 + CloudFront)

1. Uploaded all frontend files (`index.html`, `.css`, `.js`) to S3 bucket.  
2. Created a **CloudFront distribution** pointing to the bucket.  
3. Set **Default Root Object** to `index.html`.

---



Credit and inspiration from: https://www.youtube.com/watch?v=ADDG7LLS5IM
