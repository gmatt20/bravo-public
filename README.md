![Bravo](https://github.com/user-attachments/assets/2df0aaf0-c3ac-4338-9606-f036efcc377f)

## Bravo is a full-stack web application that helps users optimize their daily schedules by parsing their calendars, collecting their preferences, and outputting an optimized scheduled by an LLM. I designed both the backend API and the frontend.

## Features

- **Calendar Integration**  
  Users can upload an `.ics` file to parse existing events and constraints from the frontend.

- **Preference Engine**  
  Users can configure focus block duration, number of blocks per day, working hours, breaks, and chronotype (morning, evening, balanced). Input validation is handled via Zod.

- **Optimization Jobs**  
  Each request from the frontend creates an optimization job in the backend, linking the user's original file, preferences, and the resulting optimized schedule.

- **AI-Powered Scheduling**  
  Google Gemini restructures events into a productive daily plan while respecting user constraints and sleep preferences.

- **File Output**  
  The backend generates a new `.ics` calendar file that can be imported back into Google Calendar, Outlook, or Apple Calendar.

## Tech Stack

- **Frontend:** Next.js, React, TypeScript, ShadCN/UI, React Hook Form  
- **Backend:** Node.js, Express, Drizzle ORM, Zod  
- **Database:** PostgreSQL (Neon)
- **Authentication:** NextAuth.js  
- **Calendar Parsing & Optimization:** Custom ICS parser and AI scheduling algorithms
