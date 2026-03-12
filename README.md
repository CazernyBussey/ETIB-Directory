

ETIB Community Connect Directory

A full-stack, accessibility-first business directory for the blind and visually impaired community.

Overview

ETIB Community Connect Directory helps users discover trusted businesses that are either:

• Blind-owned / visually impaired-owned
• Community service providers specifically serving blind and visually impaired individuals
• Or both

This project includes:

• Public searchable directory
• Business owner signup/login
• Listing submission workflow
• Admin moderation dashboard
• Optional email notifications for status updates

───

Tech Stack

• Frontend: HTML, CSS, Vanilla JavaScript
• Backend: Node.js, Express
• Database: SQLite
• Auth: JWT + bcrypt
• Deployment target: Render

───

Project Structure

• public/ → Frontend pages and client scripts
• server/ → API, auth, database schema, server logic
• render.yaml → Render deployment config
• DEPLOYMENT.md → deployment walkthrough

───

Features

Public

• Browse approved listings
• Filter by category, type, location, and contact method
• View listing profile details

Business Owners

• Create account
• Sign in
• Submit listing for moderation
• View own listing statuses and admin notes

Admin

• View pending/approved/rejected/needs-changes submissions
• Approve, reject, or request changes
• Review users and reports
• Track moderation actions

───

Environment Variables

Create a .env file in server/ (or set in Render):

PORT=8080
JWT_SECRET=replace-with-a-long-random-string
ADMIN_EMAIL=eventhoughimblind@gmail.com

# Optional SMTP for notification emails
SMTP_HOST=
SMTP_PORT=587
SMTP_SECURE=false
SMTP_USER=
SMTP_PASS=
SMTP_FROM="ETIB Community Connect <no-reply@eventhoughimblind.com>"

───

Local Development

cd server
npm install
cp .env.example .env
npm start

Open:

• http://localhost:8080

───

Deployment (Render)

1. Push repo to GitHub
2. In Render, create a Web Service from this repo
3. Render uses render.yaml automatically
4. Add environment variables in Render dashboard
5. Deploy and test /api/health

───

Accessibility Priorities

• Semantic HTML structure
• Keyboard-accessible navigation
• Labeled forms and controls
• Screen-reader-friendly content flow
• Clear visual focus states

───

Security Notes

• Do not commit real secrets to GitHub
• Use strong JWT_SECRET
• Enable HTTPS in production
• Revoke any exposed tokens/passwords immediately

───

License

This project is owned and maintained by ETIB (Even Though I’m Blind, Inc.).
Use and distribution rights are managed by the organization.

───

If you want, I can also give you a short version README (cleaner for public visitors) and a separate TECHNICAL.md for developers.
Mar 11, 2026 at 9:24 PM
