#  Blood Management System (BMS)

A centralized web-based platform designed for university-level blood donor and recipient management. Developed by MCA Team B (TIET, Patiala), this system streamlines the process of blood donation and requests, ensuring accessibility, reliability, and quick response during medical emergencies.

---

##  Project Overview

**Problem Statement**  
Finding suitable blood donors during emergencies is often time-consuming and inefficient. The Blood Management System aims to create a platform that connects recipients with potential donors in real-time within the university ecosystem.

**Objective**  
To develop a website where:
- **Donors** can register/update their availability.
- **Recipients** can search and request blood based on blood group.
- **Admins** manage, verify, and monitor users and requests.

---

##  Features

###  User Authentication
- Unified login/register portal for Admins, Donors, and Recipients.
- Secure login with email/password and role-based access.

###  Donor Module
- Register with blood group, name, and contact.
- View incoming blood requests.
- Accept/Reject requests from recipients (via email interaction).
- Update profile or availability status.

###  Recipient Module
- Search for blood by selecting from dropdown of blood groups.
- View available donors filtered by blood type.
- Send blood request to matching donors (one-by-one mail requests).
- View how many donors the request was sent to.

###  Admin Module
- Add new donors or other admins.
- Edit/Delete existing donor profiles.
- Verify donor authenticity.
- Monitor all requests sent by recipients.

---

##  Email System

- When a **recipient sends a request**, each matching **donor receives a personalized email**.
- The email includes:
  - Requestor details
  - Option to **Accept** or **Reject**
- Upon donor addition, confirmation mail is sent asking if they wish to join.

---

##  Functional Requirements

| Module       | Key Functions                                                                 |
|--------------|--------------------------------------------------------------------------------|
| Donor        | Register, Update Availability, View Requests, Accept/Reject Request            |
| Recipient    | Search Donors, Send Request, View Request Status                               |
| Admin        | Add/Edit/Delete Donors & Admins, Monitor Requests                              |

---

##  Quality Attributes

- **Security:** Encrypted data, secure login.
- **Reliability:** 24/7 access, backup mechanisms in place.
- **Scalability:** Can extend beyond university to hospitals.
- **Usability:** Simple UI, mobile-friendly, intuitive interactions.

---

##  Tech Stack

- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Node.js, Express.js
- **Database:** MongoDB
- **Email Service:** Nodemailer
- **Authentication:** JWT
- **Deployment:** (Specify e.g. Heroku/Vercel/AWS if deployed)

---

##  Tools Used

| Tool         | Purpose                                         |
|--------------|--------------------------------------------------|
| MongoDB      | Store donor, recipient, and admin data          |
| Express.js   | Backend server and route handling               |
| Nodemailer   | Send email notifications and requests           |
| JWT          | Secure login & authentication                  |
| HTML/CSS/JS  | Build frontend interface                        |
| GitHub       | Version control and collaboration               |

---

##  System Architecture

```mermaid
graph LR
A[User (Donor/Recipient/Admin)] --> B[Login/Register Page]
B --> C[Role-Based Dashboard]
C --> D[MongoDB Database]
C --> E[Email Notification System (Nodemailer)]
C --> F[Request Management / Availability Updates]
