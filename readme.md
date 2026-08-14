# Expense Tracker

A simple, single-page web app for logging daily expenses and seeing where your money goes — built with plain HTML, CSS, and JavaScript (no frameworks, no build tools).

## Live demo
https://diwakarkumar2508205-jpg.github.io/Expense-Tracker/

## Features
- Add an expense with an amount, category, and note
- See a running total of all spending
- See spending broken down and sorted by category
- Delete any expense
- Data persists across page refreshes using `localStorage`

## Why I built this
I wanted a small, complete project to practice core front-end fundamentals — DOM manipulation, event handling, array methods (`reduce`, `filter`, `map`), and browser storage — without the overhead of a framework, so I could focus on understanding what's actually happening under the hood.

## Tech stack
- HTML5
- CSS3 (custom properties / CSS variables for theming)
- Vanilla JavaScript (ES6+)
- Browser `localStorage` for persistence

## How it works
- Expenses are stored as an array of objects in memory: `{ id, amount, category, note }`
- Every change (add/delete) re-renders the list and totals from that array, and saves the array to `localStorage`
- On page load, any previously saved data is loaded back in before anything is rendered
- Category totals are computed using `Array.reduce()` to group and sum expenses by category
- Delete uses event delegation: a single click listener on the list container, rather than one listener per button, so it keeps working correctly as rows are added and removed

## Running it locally
No build step needed — just open `index.html` in any browser.

## Deploying (free options)
**GitHub Pages**
1. Push this project to a GitHub repository
2. Go to Settings → Pages
3. Set the source to your main branch, root folder
4. Your app will be live at `https://<your-username>.github.io/<repo-name>/`

**Netlify**
1. Go to netlify.com and sign up (free)
2. Drag and drop this project folder onto the Netlify dashboard
3. You'll get a live URL instantly

## Possible next steps
- Edit an existing expense instead of only delete + re-add
- Filter expenses by date range
- Add a simple chart (e.g., a pie chart of category spending)
- Move storage from `localStorage` to a real backend + database
