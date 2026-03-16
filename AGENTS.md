\# Vault — AI Agent Development Guide



This document defines the rules and architecture for AI agents working on the Vault project.



Vault is a \*\*privacy-first personal finance PWA\*\* designed to work offline and store all data locally.



\---



\# Project Overview



Vault is an offline-first expense tracker and financial intelligence tool.



Core principles:



\- Privacy first

\- Offline first

\- User owned data

\- Lightweight mobile UX



\---



\# Technology Stack



Frontend:

React + Vite



Styling:

Tailwind CSS



Charts:

Chart.js



Local Storage:

IndexedDB



OCR:

Tesseract.js



Encryption:

Web Crypto API (AES-256-GCM)



Deployment:

GitHub Pages



\---



\# Architecture



The application uses layered architecture.



UI (React)

↓

Application Logic

↓

Service Layer

↓

IndexedDB

↓

Analytics Engine





Core modules:



\- transactionService

\- merchantLearningService

\- importService

\- OCRService

\- analyticsService



\---



\# Development Rules



AI agents must follow these rules.



1\. \*\*Never regenerate the entire project\*\*

2\. \*\*Only make incremental changes\*\*

3\. \*\*Do not change project structure\*\*

4\. \*\*Never overwrite critical config files\*\*



Critical files:





package.json

vite.config.js

.gitignore





These files must not be modified unless explicitly requested.



\---



\# Output Format



All AI changes must follow this structure.





CHANGES SUMMARY



FILES TO CREATE

FILES TO MODIFY





Then provide full code for each changed file.



\---



\# Database



Vault uses IndexedDB as the primary database.



All transaction data is stored locally.



Transaction schema:





id

amount

type

category

merchant

paymentMethod

date

notes

tags

createdAt

updatedAt





\---



\# Import Engine



Vault supports importing transactions from:



\- CSV

\- Excel

\- PDF

\- OCR receipts

\- Text paste



Import logic must be flexible and detect:



\- date

\- merchant

\- amount

\- debit/credit



without requiring strict formats.



\---



\# UX Principles



The UI must follow mobile-first design.



Important interactions:



\- swipe gestures for transactions

\- floating action button for quick entry

\- bottom navigation with 5 tabs

\- single tap actions where possible



Accessibility standards must be respected.



\---



\# Security



All sensitive operations must follow:



\- encrypted backups

\- secure PIN lock

\- Web Crypto API encryption



No user financial data should be sent to external services.



\---



\# AI Agent Behaviour



AI agents must:



\- read existing files before modifying them

\- avoid large rewrites

\- keep code modular

\- maintain backward compatibility



If unsure about architecture, request clarification before implementing.



\---



\# Build \& Deployment



Local development:





npm run dev





Production build:





npm run build





Deploy to GitHub Pages:





npm run deploy





\---



\# Goal



Vault should evolve into a \*\*personal financial intelligence system\*\*, not just an expense tracker.



Future roadmap includes:



\- multi-device sync

\- improved import intelligence

\- financial insights

\- anomaly detection



