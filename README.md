📥 Customer Enquiry Inbox (Cloud-Based Web Application)
📌 Project Overview

The Customer Enquiry Inbox is a cloud-based web application designed to capture, manage, and analyse customer enquiries in real time.
It demonstrates how a simple business process (customer enquiries) can be implemented using cloud-native services with real-time data synchronization.

This project was developed as part of the Doing Business on the Cloud module to showcase:

Cloud data storage

Real-time updates

Separation of user roles

Lightweight deployment using GitHub Pages

🎯 Business Problem

Many small and medium-sized businesses rely on email or spreadsheets to manage customer enquiries. This often leads to:

Delayed responses

No visibility of enquiry status

No performance insights

This project addresses the problem by providing:

A public-facing enquiry form

A real-time staff dashboard

A live insights and reporting view

🧩 Solution Architecture

The solution is divided into three independent web modules, all connected to a single cloud database.

Public User  ──► Firestore ◄── Staff Dashboard
                          ◄── Insights Dashboard


Frontend: HTML, CSS, JavaScript

Backend (Cloud): Firebase Cloud Firestore

Hosting: GitHub Pages

Data Sync: Real-time listeners (no page refresh required)

🗂️ Project Structure
Customer-Enquiry-Inbox/
│
├── index.html        # Redirects to public.html (GitHub Pages root)
├── public.html       # Public enquiry submission form
├── staff.html        # Staff dashboard (real-time management)
├── insights.html     # Live analytics and KPIs
└── README.md         # Project documentation

🧑‍💼 Application Modules
1️⃣ Public Enquiry Form (public.html)

Audience: Customers / public users

Features:

Submit name, email, and enquiry message

Data saved directly to the cloud

Automatic timestamps added

No login required

Purpose:
Captures customer enquiries and stores them in Firestore.

🔗 Live link:
/public.html

2️⃣ Staff Dashboard (staff.html)

Audience: Internal staff

Login credentials (for markers):

Username: staff

Password: nci123

Features:

View all enquiries in real time

Update enquiry status (New / In Progress / Resolved)

Add internal staff-only notes

Changes appear instantly without refresh

Purpose:
Allows staff to manage and track enquiries efficiently.

🔗 Live link:
/staff.html

3️⃣ Insights Dashboard (insights.html)

Audience: Management / operations

Features:

Total enquiries count

Status breakdown (New, In Progress, Resolved)

Enquiries created in last 24 hours

Resolution rate

Recent enquiries table

All metrics update in real time

Purpose:
Provides operational insights derived directly from live cloud data.

🔗 Live link:
/insights.html

☁️ Cloud Technologies Used
Firebase Cloud Firestore

Central cloud database

Stores all enquiries

Supports real-time listeners

Shared across all three modules

GitHub Pages

Hosts the static HTML files

No backend server required

Publicly accessible URLs

🔄 Real-Time Functionality (Key Feature)

This application uses Firestore real-time listeners, meaning:

New enquiries appear in Staff and Insights dashboards instantly

Status updates made by staff are reflected immediately in Insights

No manual refresh is required

This demonstrates a core cloud computing concept: event-driven, real-time data propagation.

🔐 Security Notes

Firebase Authentication is not used (out of scope for this project)

Staff login is implemented as a simple in-page gate for demonstration

Firestore rules are in test mode for development purposes

📈 Success Metrics

Enquiries captured successfully

Real-time updates working without refresh

Staff able to manage enquiry lifecycle

Insights accurately reflect live data

🚀 How to Run the Project

No installation required.

Open any of the live GitHub Pages links in a browser

Submit an enquiry via public.html

View and manage it in staff.html

Observe live metrics in insights.html

📚 Academic Context

This project was developed to meet the assessment requirements of:

Module: Doing Business on the Cloud (H9BOC)

Focus Areas: Cloud services, real-time data, lightweight deployment, business value
