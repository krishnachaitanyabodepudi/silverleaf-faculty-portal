<p align="center">
  <img src="/assets/Logo.png" width="150">
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
  <img src="/assets/Architectures.png" width="720">
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
  <img src="/assets/data-flow.png" width="720">
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
  <img src="/assets/erd.png" width="720">
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

# <span style="color:#003366;">Dashboard</span>

The dashboard includes:
- Submission analytics  
- Assignments per course  
- Faculty workload  
- Student performance indicators  
- AI feedback visibility  
- Timeline of submissions  


---

<span style="color:#003366;">Ethical & Social Considerations</span>
<span style="color:#008060;">Bias & Fairness</span>

Faculty oversee all AI outputs

Transparent indicators for AI usage

<span style="color:#008060;">Privacy & Security</span>

Local LM Studio avoids external data sharing

Secure data storage

<span style="color:#008060;">Accessibility</span>

Clear UI

Consistent workflows

<span style="color:#008060;">Governance</span>

FERPA & GDPR guidelines

Institution-specific AI policies

<span style="color:#003366;">Outcomes, Impact & Next Steps</span>
<span style="color:#008060;">Impact</span>

Faster grading

Reduced faculty workload

Improved clarity and student learning

AI-ready institutional environment

<span style="color:#008060;">Next Steps</span>

Pilot testing

Full deployment

Faculty & student training

LMS integration

Extended analytics

<span style="color:#003366;">Team Reflection</span>

Our team learned academic AI design, ethical guidelines, system architecture, research analysis, and the importance of aligning technology with real educational needs. We developed collaboration, communication, and system-level thinking skills while preparing Silverleaf University for an AI-enabled future.
  <source src="/assets/explain.mp4" type="video/mp4">
</video>
