🎫 HelpDesk Pro – Technical Support Ticket Management System

A complete and scalable support system built with Next.js 14, TypeScript, MongoDB, and NextAuth.

👨‍💻 Developer Information

Name: Maria VIctoria VIloria

Clan: Macondo

Email: mvviloriaanaya44@gmail.com


🚀 Main Features
✅ Complete Ticket Management

Create, edit, update, and close tickets

Status options: Open, In Progress, Resolved, Closed

Priority levels: Low, Medium, High

Agent assignment

✅ Role-Based User System

Clients: create and manage their tickets

Agents: manage all tickets

✅ Real-Time Comments

Threaded conversation per ticket

Email notifications

✅ Automated Notifications

Email when a ticket is created

Email when a new response arrives

Email when a ticket is closed

✅ Cron Jobs

Hourly reminders for inactive tickets

Daily satisfaction surveys

✅ Modern and Responsive UI

Reusable components

Dynamic status/priority badges

Mobile-friendly interface

📋 Prerequisites

Node.js 18+

MongoDB 6+

SMTP Email Account (Gmail recommended)

🛠️ Installation
1. Clone the repository
git clone https://github.com/your-user/helpdesk-pro.git
cd helpdesk-pro

2. Install dependencies
npm install

3. Configure environment variables

Create a .env.local file in the project root:

# MongoDB
MONGODB_URI=mongodb://localhost:27017/helpdesk-pro

# NextAuth
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=your-random-secret-here

# Email (Gmail)
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password


Note: For Gmail, you must generate an App Password.

4. Seed the database
npx ts-node scripts/seed.ts


This creates test users:

Role	Email	Password
Client	cliente@test.com
	password
Agent	agente@test.com
	password
5. Run the project
npm run dev


Open: http://localhost:3000



Client Dashboard – ticket list and creation

Agent Dashboard – filtering and ticket management

Ticket Details – comments and updates

Ticket Creation Form

🗂️ Project Structure
helpdesk-pro/
├── src/
│   ├── app/
│   │   ├── [locale]/
│   │   │   ├── client/          # Client dashboard
│   │   │   ├── agent/           # Agent dashboard
│   │   │   ├── login/           # Login page
│   │   │   └── page.tsx         # Home page
│   │   └── api/
│   │       ├── auth/            # NextAuth
│   │       ├── tickets/         # Tickets API
│   │       └── comments/        # Comments API
│   ├── components/
│   │   ├── tickets/             # Ticket components
│   │   ├── comments/            # Comment components
│   │   └── ui/                  # Reusable UI components
│   ├── lib/
│   │   ├── models/              # Mongoose models
│   │   ├── mongodb.ts           # DB connection
│   │   ├── auth.ts              # NextAuth config
│   │   ├── email.ts             # Email service
│   │   └── cron.ts              # Cron jobs
│   ├── services/                # Axios services
│   ├── hooks/                   # Custom hooks
│   ├── types/                   # TypeScript types
│   └── messages/                # i18n messages
├── scripts/
│   └── seed.ts                  # DB seeding script
├── .env.local
├── package.json
└── README.md

## 🔐 Roles & Permissions
Client

✅ View their own tickets

✅ Create tickets

✅ Comment on their tickets

❌ Cannot change status or priority

Agent

✅ View all tickets

✅ Filter by status/priority

✅ Update status and priority

✅ Assign tickets

✅ Add comments

✅ Close tickets

## 📧 Notification System
Automatic Emails

Ticket Created – confirmation sent to client

New Response – sent when an agent replies

Ticket Closed – closure confirmation

Cron Jobs

Hourly reminders: tickets inactive for 24 hours

Daily surveys (9 AM): feedback for recently closed tickets

## 🛠️ Technologies Used

Frontend: Next.js 14, React 18, TypeScript

Styling: Tailwind CSS

Authentication: NextAuth.js

Database: MongoDB + Mongoose

Email: Nodemailer

i18n: next-intl

HTTP Client: Axios

Cron Jobs: node-cron

Validation: Zod


## 🧪 Testing Guide
Test Accounts

Client

Email: cliente@test.com

Password: password

Agent

Email: agente@test.com

Password: password

Testing Flow
As Client:

Log in

Create a ticket

View it in the dashboard

Add a comment

As Agent:

Log in

See all tickets

Filter by status

Open the client’s ticket

Change status to In Progress

Reply with a comment

Mark as Resolved

Close the ticket

Verify Emails:

Check inbox

Confirm all notifications arrived

🐛 Troubleshooting
MongoDB connection errors
sudo systemctl status mongod
sudo systemctl start mongod

Emails not sending

Check EMAIL_USER and EMAIL_PASS

For Gmail: use an App Password

Inspect server logs

Authentication issues

Ensure NEXTAUTH_SECRET is set

Clear browser cookies

Restart the server

## 📝 Available Scripts
npm run dev       # Development server
npm run build     # Production build
npm run start     # Start production
npm run lint      # Run linter

## Deployment (Vercel Recommended)

Push project to GitHub

Import into Vercel

Add environment variables

Deploy

Production Environment Variables
MONGODB_URI=...
NEXTAUTH_URL=https://your-domain.com
NEXTAUTH_SECRET=...
EMAIL_HOST=...
EMAIL_PORT=...
EMAIL_USER=...
EMAIL_PASS=...


## 🤝 Contributing

Fork the repository

Create a feature branch

git checkout -b feature/new-feature


Commit changes

Push the branch

Open a Pull Request



## 📄 License

This project is licensed under the MIT License.






For questions or suggestions:

Email: mvviloriaanaya44gmail.com

GitHub: [@Mvicky027]
