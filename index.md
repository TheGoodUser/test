# Screening Assignment

## 🎯 Objective

This assignment is designed to evaluate your ability to:

* Build a **mobile application** (React Native or Flutter)
* Create and integrate a **backend API**
* Work with **REST APIs**
* Handle **file uploads**
* Store and retrieve data using a **database (MySQL or PostgreSQL)**

---

## 🧩 Problem Statement

You are required to build a simple mobile application that allows users to:

1. Upload an image
2. Send the image to your own backend server
3. Your backend will forward the image to a provided AI API
4. Receive a response (video URL) from the AI API
5. Store the request and response in a database
6. Display the result in the mobile app

---

## 🔌 AI API Details (Provided)

**Endpoint:**

```
https://fatmachines.com/assignment/ai.php
```

**Method:**
`POST`

**Headers:**

```
X-Auth-Key: abcdefghijklmnop
```

**Response:**

```json
{
  "success": true,
  "output": "https://fatmachines.com/assignment/ai.mp4"
}
```

---

## 🏗️ Requirements

### 1. Mobile App (Frontend)

You can use:

* React Native **or**
* Flutter

#### Features:

* Select or capture an image
* Upload image to your backend
* Show loading state while processing
* Display the returned video (URL)
* Show previous uploads (history list)

---

### 2. Backend API

You can use:

* PHP, Python, Golang, Node.js, or any backend language

#### Responsibilities:

* Accept image upload from mobile app
* Forward request to the provided AI API
* Handle authentication header
* Return API response to the mobile app

#### Suggested Endpoint:

```
POST /upload
```

> You may run your backend locally (e.g., `localhost`) or host it anywhere.

---

### 3. Database

Use:

* MySQL **or**
* PostgreSQL

#### Suggested Schema:

Table: `requests`

| Field      | Type      | Description           |
| ---------- | --------- | --------------------- |
| id         | integer   | Primary key           |
| image_url  | text      | Uploaded image path   |
| output_url | text      | AI response video URL |
| created_at | timestamp | Request timestamp     |

---

### 4. Flow Overview

1. User selects image in app
2. App uploads image to backend
3. Backend:

   * Receives image
   * Calls AI API with header auth
   * Gets response
   * Stores record in DB
4. Backend returns result to app
5. App displays video and history

---

## ⏱️ Time Limit

* Expected completion time: **2 hours**
* Focus on functionality over perfection

---

## ✅ Evaluation Criteria

| Criteria        | What We Look For                       |
| --------------- | -------------------------------------- |
| Code Quality    | Clean, readable, structured code       |
| Architecture    | Logical separation of frontend/backend |
| API Integration | Correct usage of REST APIs             |
| Database Usage  | Proper schema and storage              |
| UX              | Basic but functional UI                |
| Error Handling  | Handles failures gracefully            |

---

## 🚀 Bonus (Optional)

* Image preview before upload
* Retry mechanism on failure
* Pagination for history
* Clean UI/UX improvements

---

## 📦 Submission Guidelines

Please provide:

1. A **working demo video** of your application
2. Upload the video to **Google Drive** with public access
3. Share the **Google Drive link**

> The app can run on **localhost or any hosted server** — both are acceptable.

---

## 🔒 Code Privacy

To maintain your privacy:

* You **do not need to share your source code or GitHub repository**
* We will only ask for code access if required in later stages

---

## ⚠️ Notes

* You must use your own backend (**direct API calls from mobile are not allowed**)
* Keep implementation simple and focused
* You are free to use any libraries/frameworks

---

## 💡 Goal

We are not expecting a perfect production-ready app.
We want to see how you:

* Structure your code
* Think through the problem
* Implement core features under time constraints

---

Good luck! 🚀
