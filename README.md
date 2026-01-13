# TaskGlitch – Bug Fixes Assignment

This repository contains my solution for the **TaskGlitch Bug Fixes Challenge**.  
The task was to analyze an existing React + TypeScript application and fix multiple bugs related to logic, UI behavior, and performance.

---

## 🚀 Live Demo

🔗 **Live App:** https://task-glitch-indol.vercel.app/  
🔗 **GitHub Repo:** https://github.com/vamshigithubm/task-glitch

---

## 🧠 Assignment Objective

Fix critical issues in a task management app used by sales teams to track tasks based on **ROI (Revenue ÷ Time Taken)**, while ensuring the app is:

- Stable
- Deterministic
- User-friendly
- Free of UI glitches and invalid calculations

---

## 🐞 Bugs Fixed

### ✅ Bug 1 – Double Data Fetch on Load
- Issue: Tasks were fetched twice on initial render.
- Fix: Removed redundant `useEffect` and ensured data loads only once.
- Result: No duplicated tasks, clean console logs.

---

### ✅ Bug 2 – Undo Snackbar State Bug
- Issue: Deleted tasks could reappear incorrectly after snackbar auto-close.
- Fix: Cleared `lastDeleted` state when snackbar closes.
- Result: Undo works only within the active snackbar window.

---

### ✅ Bug 3 – Unstable Sorting (Flickering Order)
- Issue: Tasks with same ROI and priority reordered randomly.
- Fix: Added a deterministic tie-breaker using task title.
- Result: Stable, predictable sorting on every render.

---

### ✅ Bug 4 – Double Dialog Opening
- Issue: Clicking Edit/Delete also triggered the row’s View dialog.
- Fix: Stopped event bubbling using `event.stopPropagation()`.
- Result: Each action opens only its intended dialog.

---

### ✅ Bug 5 – ROI Calculation Errors
- Issue: ROI showed `NaN` / `Infinity` for invalid inputs.
- Fix: Added validation to prevent division by zero or invalid numbers.
- Result: Safe ROI calculations with clean UI and analytics.

---

## 🛠️ Tech Stack

- **React 18**
- **TypeScript**
- **Vite**
- **Material UI**
- **Tailwind CSS**

---

## 📦 How to Run Locally

```bash
npm install
npm run dev

---

🎯 Key Learnings  

Debugging real-world React bugs

Safe mathematical computations

Deterministic sorting for UI stability

Proper event handling (event bubbling)

Clean state management for undo operations

---

📌 Submission Notes

All fixes are committed with clear messages.

App is deployed and tested in incognito mode.

No backend used (local/in-memory state only).
