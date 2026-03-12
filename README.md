# Backend Project Setup Guide

এই গাইডটি অনুসরণ করে আপনি নতুন একটি কম্পিউটারে GitHub থেকে প্রজেক্ট Clone করে Backend সহজে Run করতে পারবেন।

---

## 1. প্রয়োজনীয় Software Install
প্রথমে নিচের সফটওয়্যারগুলো আপনার কম্পিউটারে Install থাকতে হবে:

- **Node.js** – Backend রান করার জন্য
- **Git** – GitHub থেকে Project Clone করার জন্য
- **XAMPP** – MySQL Database ব্যবহার করার জন্য

---

## 2. Project Clone করা
GitHub থেকে Project Download করার জন্য নিচের Command ব্যবহার করুন:

```
git clone https://github.com/your-username/your-repo.git
```

তারপর Project Folder এ প্রবেশ করুন:

```
cd your-repo
```

---

## 3. Environment File তৈরি করা
Project এর Root Folder এ একটি **.env** ফাইল তৈরি করুন।

উদাহরণ:

```
DATABASE_URL="mysql://root:@localhost:3306/your_database_name"
PORT=5000
```

এখানে Database Name আপনার প্রয়োজন অনুযায়ী পরিবর্তন করতে হবে।

---

## 4. XAMPP Start করা
XAMPP Control Panel ওপেন করে নিচের সার্ভিসগুলো Start করুন:

- Apache
- MySQL

Database চালু না থাকলে Backend Database এর সাথে Connect করতে পারবে না।

---

## 5. Dependencies Install
Project এর সব প্রয়োজনীয় Package Install করার জন্য নিচের Command চালান:

```
npm install
```

এটি package.json ফাইল দেখে সব Node Modules Install করবে।

---

## 6. Prisma Client Generate
Prisma ORM ব্যবহার করলে Client Generate করতে হবে:

```
npx prisma generate
```

এটি Prisma Schema অনুযায়ী Database Client তৈরি করে।

---

## 7. Database Sync করা
Database Schema Database এ Push করার জন্য নিচের Command ব্যবহার করুন:

যদি Migration না থাকে:

```
npx prisma db push
```

যদি Migration থাকে:

```
npx prisma migrate dev
```

এতে Database Table গুলো Automatically তৈরি হয়ে যাবে।

---

## 8. Backend Run করা
সবকিছু Setup হয়ে গেলে Backend Server চালু করুন:

```
npm run dev
```

Server সাধারণত নিচের Address এ Run করবে:

```
http://localhost:5000
```

---

# Quick Command Summary

```
git clone https://github.com/your-username/your-repo.git
cd your-repo
npm install
npx prisma generate
npx prisma db push
npm run dev
```

---

✅ এখন আপনার Backend Project নতুন কম্পিউটারেও সফলভাবে Run করবে।

