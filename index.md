<p align="center">
  <img src="assets/Logo.png" width="150">
</p>

<h1 align="center" style="color:#003366; font-size: 36px; margin-bottom:0;">
  Silver Leaf University – Faculty & Student Portal
</h1>

<p align="center" style="font-size:18px; color:#0059b3; margin-top:4px;">
  Team 4: Modern Research Pioneers
</p>

<p align="center">
  Akshaya Cheruku • Gowri Bhavani Bommareddy • Krishna Chaitanya Bodepudi • Krishna Chaitanya Nizam • Sai Tulasi Akarapu
</p>

---

<div align="center" style="font-size:17px; font-weight:600; margin-bottom:12px;">


</div>

---

# <span style="color:#003366;">Executive Summary</span>

Silverleaf University is preparing for a major shift in how its faculty operate by introducing AI-powered tools and updated teaching technologies. As the Modern Research Pioneers (MRP) team, we focused on building a solution that helps faculty feel more confident using AI while also easing their workload. Our idea is a support portal that offers syllabus-aligned AI Faculty Support tools that assist with grading, class preparation, and quick academic assistance through a conversational AI trained specifically on Silverleaf University’s content.

Through research, system design analysis, and academic insight, our project aims to save faculty time, increase support efficiency, and help the university adopt a responsible, scalable, AI-ready academic ecosystem. The solution addresses operational challenges by aligning course design with AI models, delivering fast feedback to students, and providing faculty with structured and customizable AI support.

The system integrates the Gemini API for cloud-based AI and LM Studio for private local inference to ensure secure, policy-compliant usage. Our platform represents a modern and ethical approach to AI-powered academic support—balancing innovation, governance, transparency, and educational value.

---

# <span style="color:#003366;">Problem Context & Stakeholder Perspectives</span>

Faculty at Silverleaf University manage increasing academic expectations while navigating new teaching technologies. Many feel overwhelmed by administrative tasks, unclear workflows, and the lack of AI systems trained specifically on their syllabi and course structures. Students require consistent guidance, timely feedback, and structured academic support. Administrators must manage compliance, content governance, and institutional AI adoption.

Universities are also under pressure to modernize digital infrastructure, deliver AI-enabled learning experiences, and maintain competitive academic programs while ensuring responsible governance.

## <span style="color:#0059b3;">Stakeholders</span>

### <span style="color:#008060;">Faculty</span>
- Require support with grading, feedback, example generation  
- Need syllabus-aligned academic AI tools  
- Want faster ways to handle content-heavy tasks  

### <span style="color:#008060;">Students</span>
- Expect quick feedback  
- Need clarity on assignments and course structure  
- Benefit from consistent academic support  

### <span style="color:#008060;">Administrators</span>
- Oversee course-to-faculty mapping  
- Maintain oversight of academic operations  
- Ensure compliance and policy governance  

---

# <span style="color:#003366;">Research & Insights</span>

Our research used EDUCAUSE, Gartner, Ithaka S+R studies, and Deloitte’s AI in Education reports. Key findings:

- Students increasingly depend on AI for study assistance  
- Automated feedback saves faculty significant time  
- Universities must ensure governance, explainability, and policy alignment  
- Ethical issues include data privacy, bias mitigation, and transparency  
- Conversational AI can support learning if aligned with curriculum  
- Academic institutions prefer internal or private AI models for security  

We examined market tools like Cognigy and Kore.ai to understand workflow automation, but our academic problem required a custom-built syllabus-aligned system.

---

# <span style="color:#003366;">Proposed Solution</span>

The **AI Faculty Support Portal** is a centralized solution that assists faculty, students, and administrators with teaching workflows, academic communication, AI-based learning support, and grading assistance.

### <span style="color:#008060;">Core Components</span>

#### **1. Course-Aligned AI Assistant**
AI chatbot trained on:
- Syllabi  
- Rubrics  
- Reading material  
- Course outcomes  

Supports:
- Class preparation  
- Example generation  
- Assignment guidance  
- Clarification of concepts  

#### **2. AI Feedback Analyzer**
- Uses Gemini API  
- Analyzes PDF submissions  
- Extracts context  
- Generates preliminary feedback  
- Helps faculty save grading time  

#### **3. Assignment Workflow System**
- Admin assigns courses to faculty  
- Faculty create assignments  
- Students upload PDF submissions  
- AI & faculty feedback stored in the portal  

#### **4. Secure, Compliant AI Infrastructure**
Supports:
- Local LM Studio (Llama models / Private inference)  
- Cloud Gemini API (High-power inference)  

---

# <span style="color:#003366;">Enterprise Architecture</span>

<p align="center">
  <img src="assets/Architectures.png" width="720">
</p>

### <span style="color:#008060;">Business Architecture</span>
- Differentiated workflows for admin, faculty, and students  
- Assignment, submission, AI feedback, and communication workflows  

### <span style="color:#008060;">Information System Architecture</span>
- Academic content flow  
- AI integration layer  
- Syllabus → AI Model → Feedback → Dashboard  

### <span style="color:#008060;">Technology Architecture</span>
- Next.js, TypeScript, Tailwind, shadcn/ui  
- Node.js/Next API endpoints  
- Gemini API & LM Studio models  

---

# <span style="color:#003366;">Data Design</span>

<p align="center">
  <img src="assets/data-flow.png" width="720">
</p>

### <span style="color:#008060;">Data Flow</span>
1. Admin creates faculty & course assignments  
2. Faculty uploads assignments  
3. Students submit PDFs  
4. System extracts text  
5. Gemini API analyzes submission  
6. AI feedback + faculty feedback saved  
7. Dashboard visualizes performance  

---

# <span style="color:#003366;">Entity Relationship Diagram (ERD)</span>

<p align="center">
  <img src="assets/erd.png" width="720">
</p>

### <span style="color:#008060;">Entities</span>
- Admin  
- Faculty  
- Student  
- Course  
- Assignment  
- Submission  
- AI Feedback  
- Communication Logs  

---

## <span style="color:#003366;">Dashboard & Data Analysis</span>

Our dashboard is designed to give a quick, straightforward view of what’s happening inside each course. We didn’t overcomplicate it — the goal was to help faculty and students find the most important information without clicking through multiple screens.

### <span style="color:#008060;">What You Can See on the Dashboard</span>

- **Assignments Overview**  
  Faculty can see all assignments created for their courses at a glance.

- **Submission Status**  
  The dashboard shows how many students submitted, who is pending, and whether any submissions were late.

- **AI Feedback Visibility**  
  Whenever Gemini generates draft feedback for a PDF submission, faculty can quickly spot which assignments already have AI feedback and which ones still need review.

- **Student View**  
  Students get a clean timeline of:
  - Upcoming deadlines  
  - Past submissions  
  - Course announcements  
  - Feedback (AI + faculty review)

### <span style="color:#008060;">Why the Dashboard Matters</span>
Instead of jumping between emails, PDFs, or multiple URLs, everything related to a course is visible in one place. This saves time for faculty and reduces confusion for students.

### <span style="color:#008060;">Live Portal (Vercel Deployment)</span>
You can explore the working portal here:

🔗 **Live Prototype:**  
https://faculty-portal-mrp.vercel.app

This live link demonstrates the entire workflow — assignments, submissions, dashboard analytics, and the AI features we built into the platform.
# <span style="color:#003366;">Ethical & Social Considerations</span>

Ethical thinking was part of our project from the very beginning. Since we are using AI in an academic environment, we made sure our design respects fairness, privacy, and transparency at every stage.

### <span style="color:#008060;">Bias Mitigation</span>
All AI-generated feedback is reviewed by faculty before being shared with students. This keeps grading fair and prevents the AI from making decisions on its own.

### <span style="color:#008060;">Transparency</span>
Whenever AI assists in generating feedback or responses, the system makes it clear. Faculty always know which parts came from the model and which parts were added manually.

### <span style="color:#008060;">Privacy Protection</span>
To keep student data safe, we support running the AI locally using **LM Studio**, which ensures that submissions and text never leave the university’s environment. No external data sharing occurs during local execution.

### <span style="color:#008060;">Accessibility</span>
We kept the interface clean and straightforward so both faculty and students can use it comfortably, regardless of technical experience. The portal design supports inclusive access for different user needs.

### <span style="color:#008060;">Compliance</span>
The system design aligns with important academic and legal frameworks, including **FERPA**, **GDPR**, and Silver Leaf University’s internal AI policy. This ensures our solution remains responsible and institution-ready.

Overall, the portal incorporates fairness, accountability, and explainability into the way it works, making the use of AI supportive — not risky — in a real academic setting.
# <span style="color:#003366;">Lessons Learned & Team Reflection</span>

### <span style="color:#008060;">Team Reflection</span>

Throughout this semester, our team got hands-on experience with real AI product development — not just the technical side, but also the research, design, and ethical thinking that go into building an academic tool. We realized very early that supporting faculty with AI isn’t just about writing code. It requires trust, clear communication, and a design that respects how instructors actually work.

Working together helped us refine our ideas, test different approaches, and find a balance between what is innovative and what is actually practical. We also learned that good technology decisions come from understanding real user needs — not from following trends.

Overall, this project gave us a stronger appreciation for how AI can responsibly support higher education when it's designed carefully, transparently, and with the end users truly in mind.
# <span style="color:#003366;">Appendix</span>

### <span style="color:#008060;">GitHub Repository</span>

Here is the full codebase for our Master’s Research Project, including the frontend, backend, dataset files, and the AI integration workflow.

🔗 **GitHub Repository:**  
https://github.com/krishnachaitanyabodepudi/faculty-Portal-MRP

---

### <span style="color:#008060;">Project Walkthrough Videos</span>

Below are the two Loom videos that walk through the portal, the workflows, and the AI components. These videos show how the system works end-to-end, including assignment posting, student submissions, and the AI feedback flow.

#### **Project Walkthrough – Part 1**

<iframe 
  src="https://www.loom.com/embed/b6724a2f4ce4469192720fa2fe27cad9"
  width="100%" 
  height="400" 
  frameborder="0" 
  allowfullscreen>
</iframe>

<br><br>

#### **Project Walkthrough using LM STUDIO – Part 2**

<iframe 
  src="https://www.loom.com/embed/b394a6d672544c3781d50854da318dd9"
  width="100%" 
  height="400" 
  frameborder="0" 
  allowfullscreen>
</iframe>
