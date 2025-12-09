---
layout: default
title: Proposed Solution
---

<div class="content-section">
  <h1 class="section-title">Proposed Solution</h1>
  
  <p>The <strong>AI Faculty Support Portal</strong> is a centralized solution that assists faculty, students, and administrators with teaching workflows, academic communication, AI-based learning support, and grading assistance.</p>
  
  <h2 class="subsection-title">Core Components</h2>
  
  <div class="info-box">
    <h3 class="subsubsection-title">1. Course-Aligned AI Assistant</h3>
    <p>A conversational AI chatbot that dynamically uses course syllabi as context to provide faculty with academic support:</p>
    
    <h4>Context Integration:</h4>
    <ul>
      <li>Automatically loads and uses course-specific syllabus content</li>
      <li>Provides context-aware responses based on the selected course</li>
      <li>Expands beyond syllabus when academically relevant</li>
    </ul>
    
    <h4>Capabilities:</h4>
    <ul>
      <li>Class preparation assistance and lecture planning support</li>
      <li>Assignment guidance and clarification</li>
      <li>Deep academic explanations with examples</li>
      <li>Concept clarification and theoretical breakdowns</li>
      <li>Course topic exploration and academic expansions</li>
    </ul>
    
    <h4>Technical Implementation:</h4>
    <ul>
      <li>Uses Google Gemini 2.0 Flash API</li>
      <li>Streams responses in real-time</li>
      <li>Maintains conversation context across multiple exchanges</li>
      <li>Restricted to academic topics (filters non-academic queries)</li>
    </ul>
  </div>
  
  <div class="info-box">
    <h3 class="subsubsection-title">2. AI Feedback Analyzer</h3>
    <p>An automated grading assistance system that analyzes student submissions and generates structured feedback:</p>
    
    <h4>Analysis Process:</h4>
    <ul>
      <li>Processes PDF submissions in batch mode</li>
      <li>Extracts text content from uploaded PDFs</li>
      <li>Uses rubric criteria and course syllabus as evaluation context</li>
      <li>Generates preliminary feedback for faculty review</li>
    </ul>
    
    <h4>Output Features:</h4>
    <ul>
      <li>Per-student detailed feedback with strengths and areas for improvement</li>
      <li>Estimated scores (0-100) as indicators (not official grades)</li>
      <li>Error detection and issue identification</li>
      <li>Rubric-aligned evaluation across all criteria</li>
      <li>Overall summary for batch submissions</li>
    </ul>
    
    <h4>PDF Annotation:</h4>
    <ul>
      <li>Generates annotated PDFs combining original submission with feedback</li>
      <li>Highlights errors and issues in the submission</li>
      <li>Includes detailed feedback report as separate pages</li>
      <li>Downloadable annotated PDFs for each student</li>
    </ul>
    
    <h4>Time Savings:</h4>
    <ul>
      <li>Batch processing of multiple submissions simultaneously</li>
      <li>Consistent rubric-based evaluation</li>
      <li>Reduces faculty workload while maintaining quality control</li>
    </ul>
  </div>
  
  <div class="info-box">
    <h3 class="subsubsection-title">3. Assignment Workflow System</h3>
    <p>A complete end-to-end assignment management system:</p>
    
    <h4>Admin Layer:</h4>
    <ul>
      <li>Admin portal for course-to-faculty mapping</li>
      <li>View all faculty members and their assigned courses</li>
      <li>Create new courses and assign them to faculty</li>
      <li>Upload syllabus files and course materials</li>
      <li>Track course enrollment and student strength</li>
    </ul>
    
    <h4>Faculty Layer:</h4>
    <ul>
      <li>Create assignments with detailed requirements</li>
      <li>Set deliverables, submission instructions, and formatting requirements</li>
      <li>Define rubrics with weighted criteria and evaluation indicators</li>
      <li>Set due dates, maximum scores, and assignment weights</li>
      <li>View all assignments for each course</li>
      <li>Track submission status and deadlines</li>
    </ul>
    
    <h4>Student Layer:</h4>
    <ul>
      <li>View all assignments for enrolled courses</li>
      <li>Upload PDF submissions through the portal</li>
      <li>Track submission status and submission history</li>
      <li>View assignment requirements and instructions</li>
      <li>Access course-specific announcements</li>
    </ul>
    
    <h4>Data Flow:</h4>
    <ul>
      <li>Submissions stored with metadata (student ID, timestamp, course/assignment context)</li>
      <li>PDF files and extracted text stored for analysis</li>
      <li>Feedback records linked to submissions, assignments, and students</li>
      <li>Complete audit trail of all academic activities</li>
    </ul>
  </div>
  
  <div class="info-box">
    <h3 class="subsubsection-title">4. Communication & Messaging System</h3>
    <p>Dual-mode communication platform for academic interactions:</p>
    
    <h4>Course Announcements:</h4>
    <ul>
      <li>Faculty can post course-specific announcements</li>
      <li>Students see announcements in their enrolled courses</li>
      <li>Read-only view for students, full management for faculty</li>
      <li>Timestamped announcements with sender information</li>
    </ul>
    
    <h4>Direct Messaging:</h4>
    <ul>
      <li>Faculty Mail tab: Compose messages to any recipient email</li>
      <li>Student Mailbox: Send messages to faculty/support</li>
      <li>Message history tracking (sent and received)</li>
      <li>Subject and message body support</li>
      <li>Optional file attachments</li>
    </ul>
    
    <h4>Features:</h4>
    <ul>
      <li>Centralized communication hub</li>
      <li>Course-specific and global messaging</li>
      <li>Message filtering by sender/recipient</li>
      <li>Recent messages display</li>
    </ul>
  </div>
  
  <div class="info-box">
    <h3 class="subsubsection-title">5. Role-Based Access Control</h3>
    <p>Secure authentication and authorization system:</p>
    
    <h4>Three User Roles:</h4>
    <ul>
      <li>Faculty: Access to assigned courses, feedback analyzer, chatbot, announcements</li>
      <li>Students: Access to enrolled courses, assignment submission, announcements, mailbox</li>
      <li>Administrators: Access to faculty management, course assignment, system oversight</li>
    </ul>
    
    <h4>Security Features:</h4>
    <ul>
      <li>Password-based authentication (SHA-256 hashing)</li>
      <li>Role-based UI rendering</li>
      <li>API route protection by user role</li>
      <li>Session management via localStorage</li>
      <li>Secure API key handling (server-side only)</li>
    </ul>
  </div>
  
  <div class="info-box">
    <h3 class="subsubsection-title">6. Secure, Compliant AI Infrastructure</h3>
    <p>Flexible AI deployment architecture supporting multiple inference options:</p>
    
    <h4>Cloud-Based AI (Current Implementation):</h4>
    <ul>
      <li>Google Gemini 2.0 Flash API for high-power inference</li>
      <li>Server-side API routes ensure API keys never exposed to frontend</li>
      <li>Streaming responses for real-time interaction</li>
      <li>High-capacity processing for batch operations</li>
    </ul>
    
    <h4>Private Local Inference (Implemented):</h4>
    <ul>
      <li>LM Studio integration for Llama models</li>
      <li>Private inference ensures student data never leaves university environment</li>
      <li>No external data sharing during local execution</li>
      <li>Policy-compliant usage for sensitive academic data</li>
    </ul>
    
    <h4>Compliance & Governance:</h4>
    <ul>
      <li>Design aligned with FERPA (Family Educational Rights and Privacy Act)</li>
      <li>GDPR compliance considerations</li>
      <li>Institutional AI policy alignment</li>
      <li>Transparency: Clear indication of AI-generated content</li>
      <li>Bias mitigation: Faculty review required before sharing feedback</li>
      <li>Privacy protection: Support for local execution prevents data leakage</li>
    </ul>
  </div>
  
  <div class="info-box">
    <h3 class="subsubsection-title">7. Syllabus Management System</h3>
    <p>Comprehensive course content management:</p>
    
    <h4>Syllabus Storage:</h4>
    <ul>
      <li>Text-based syllabus files stored per course</li>
      <li>PDF versions available for download</li>
      <li>Syllabus content dynamically loaded for AI context</li>
      <li>Integration with chatbot and feedback analyzer</li>
    </ul>
    
    <h4>Features:</h4>
    <ul>
      <li>Syllabus viewer in course detail pages</li>
      <li>PDF download functionality</li>
      <li>Content extraction for AI context injection</li>
      <li>Course-specific syllabus association</li>
    </ul>
  </div>
  
  <div class="info-box">
    <h3 class="subsubsection-title">8. Dashboard & Analytics</h3>
    <p>Centralized view of academic activities:</p>
    
    <h4>Faculty Dashboard:</h4>
    <ul>
      <li>"My Courses" view with course duration and student count</li>
      <li>Assignment overview for all courses</li>
      <li>Submission status tracking (submitted, pending, late)</li>
      <li>AI feedback visibility indicators</li>
      <li>Quick access to all course features</li>
    </ul>
    
    <h4>Student Dashboard:</h4>
    <ul>
      <li>Course grid showing all enrolled subjects</li>
      <li>Upcoming deadlines timeline</li>
      <li>Past submissions history</li>
      <li>Course announcements feed</li>
      <li>Feedback visibility (AI + faculty review)</li>
    </ul>
    
    <h4>Admin Dashboard:</h4>
    <ul>
      <li>Faculty overview with course counts</li>
      <li>Course-to-faculty mapping visualization</li>
      <li>Enrollment tracking</li>
      <li>System-wide academic operations oversight</li>
    </ul>
  </div>
  
  <h2 class="subsection-title">Technical Architecture</h2>
  
  <div class="info-box">
    <h3 class="subsubsection-title">Frontend:</h3>
    <ul>
      <li>Next.js 15 (App Router) with React 19</li>
      <li>TypeScript for type safety</li>
      <li>Tailwind CSS + shadcn/ui component library</li>
      <li>Responsive design with dark mode support</li>
    </ul>
  </div>
  
  <div class="info-box">
    <h3 class="subsubsection-title">Backend:</h3>
    <ul>
      <li>Next.js Serverless API Routes</li>
      <li>PDF processing with pdf-parse and pdf-lib</li>
      <li>File system storage (prototype) / Ready for database migration</li>
      <li>JSON-based data storage (easily migratable to PostgreSQL)</li>
    </ul>
  </div>
  
  <div class="info-box">
    <h3 class="subsubsection-title">AI Integration:</h3>
    <ul>
      <li>Google Generative AI SDK (@google/generative-ai)</li>
      <li>LM Studio for local inference</li>
      <li>Server-side AI processing for security</li>
      <li>Streaming responses for better UX</li>
    </ul>
  </div>
  
  <div class="info-box">
    <h3 class="subsubsection-title">Deployment:</h3>
    <ul>
      <li>Vercel serverless platform</li>
      <li>Environment variable management</li>
      <li>CDN for static assets</li>
      <li>Scalable architecture ready for production</li>
    </ul>
  </div>
</div>

