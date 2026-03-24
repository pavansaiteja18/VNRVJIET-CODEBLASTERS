We built a frontend prototype called **ShaktiAI** using React 18 inside a single HTML file. It currently contains UI-only simulated features like login, AI mentor responses, eligibility engine, and document locker.

 We want to convert this into a **production-ready full-stack MERN application** with authentication, database storage, and real-time AI responses.

Please generate a complete implementation plan and working code structure for the following:

---

PROJECT GOAL

Convert my React 18 single-file frontend into:

Frontend:
React 18 + Vite or Next.js

Backend:
Node.js + Express

Database:
MongoDB

Realtime:
Socket.IO

AI integration:
OpenAI API

File storage:
MongoDB GridFS OR Firebase Storage

---

AUTHENTICATION SYSTEM REQUIREMENTS

Implement full authentication using:

JWT-based login system

Signup fields:
name
phone number
password
state
business type

Login using phone + password

Hash passwords using bcrypt

Create routes:

POST /auth/signup
POST /auth/login
GET /auth/profile

Protect routes using middleware:

verifyJWT

Store user data inside MongoDB:

UserSchema

---

DATABASE SCHEMA DESIGN

Create MongoDB schemas for:

User

Documents

Schemes

Applications

Transactions

LearningProgress

Example:

UserSchema:

name
phone
password
state
businessType
documentsUploaded
schemeMatches
eligibilityScore
createdAt

---

DOCUMENT LOCKER IMPLEMENTATION

Allow uploading:

aadhaar
pan
income certificate
caste certificate
bank passbook
photo

Store files using:

GridFS OR Firebase Storage

Create routes:

POST /documents/upload
GET /documents/user
DELETE /documents/remove

Auto-calculate:

document readiness percentage

---

SCHEME MATCHING ENGINE

Create scheme dataset JSON example:

Mudra Loan
PM Vishwakarma
Stand-Up India
Women Entrepreneurship Platform

Build eligibility logic using:

income
gender
location
category
occupation

Create route:

POST /schemes/match

Return:

eligible schemes
missing documents
confidence score

---

AI MENTOR IMPLEMENTATION

Replace simulated mentor responses with:

OpenAI API integration

Create route:

POST /mentor/chat

Send:

user message
language

Return:

AI-generated answer

Support:

English
Hindi
Telugu

---

BUSINESS PLAN GENERATOR

Create endpoint:

POST /ai/business-plan

Send:

business idea
budget
location

Return:

AI-generated structured business plan

---

REALTIME FEATURES USING SOCKET.IO

Implement:

live eligibility updates
live scheme matches
live notification alerts
mentor typing indicator
application progress updates

Create socket events:

scheme:update
mentor:typing
documents:uploaded
application:status

---

ADMIN PANEL BACKEND

Create routes:

POST /admin/add-scheme
PUT /admin/update-scheme
DELETE /admin/delete-scheme
GET /admin/users

Admin authentication required

---

PROJECT STRUCTURE REQUIRED

Generate this folder structure:

client/
server/

Inside server:

controllers/
models/
routes/
middleware/
config/
utils/

Inside client:

components/
pages/
services/
context/
hooks/

---

ENV VARIABLES REQUIRED

Generate .env example file:

MONGO_URI
JWT_SECRET
OPENAI_API_KEY
PORT

---

DEPLOYMENT SUPPORT

Prepare project for deployment on:

Frontend:
Vercel

Backend:
Railway OR Render

Database:
MongoDB Atlas

---

IMPORTANT

My frontend already exists inside a single HTML file using React 18 CDN scripts.

Help me migrate it properly into a modular React project without breaking UI functionality.

Return:

step-by-step migration plan
backend code
schema definitions
API routes
socket integration
deployment instructions
