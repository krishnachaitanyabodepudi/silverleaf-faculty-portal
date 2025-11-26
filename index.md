# Silver Leaf University – Faculty & Student Portal

**Team**: Silver Leaf Innovators  
**Members**: Member 1, Member 2, Member 3, Member 4, Member 5  

**Live Prototype**:  
[https://faculty-portal-mrp.vercel.app](https://faculty-portal-mrp.vercel.app)

**Application Code (GitHub)**:  
[https://github.com/krishnachaitanyabodepudi/faculty-Portal-MRP](https://github.com/krishnachaitanyabodepudi/faculty-Portal-MRP)

---

## Executive Summary

Silver Leaf University currently manages courses, assignments, submissions, and feedback through a mix of email, spreadsheets, and scattered LMS exports. Faculty waste time hunting for information, students are unsure about deadlines and feedback, and administrators have limited visibility into how students are performing across the program.

Our project delivers a unified **Faculty & Student Portal** that centralizes these flows. Faculty can log in, see all their courses, create and delete assignments, run AI‑assisted feedback analysis on student submissions, post course‑specific announcements, and communicate with students through a built‑in mailbox. Students see a clear dashboard of their enrolled courses, submit assignments as PDFs, check submission status, read announcements, and send mail to faculty or support.

Technically, the prototype is built with **Next.js** (full‑stack React), **TypeScript**, **Tailwind + shadcn/ui** for the interface, and **Google Gemini 2.0 Flash** for the chatbot and feedback analysis. Data is stored in structured JSON files under a `dataset/` folder which behave like a lightweight database for this Master’s Research Project. Submissions are saved as PDFs with extracted text; announcements and mailbox messages are tracked as records in a dedicated JSON collection.

The portal demonstrates how a university can move from fragmented, manual workflows to a single, role‑aware interface. It showcases end‑to‑end architecture, data design, dashboards, and AI integration that support faculty workload, improve feedback quality, and give students a more transparent and consistent experience.
