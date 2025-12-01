---
layout: default
title: Architecture & Data Design
permalink: /architecture/
---

# Architecture & Data Design

## Enterprise Architecture Overview

The Silverleaf Faculty Portal follows a modern, three-tier architecture pattern with clear separation between presentation, business logic, and data layers.

### High-Level Architecture

```
┌─────────────────────────────────────────────────────────┐
│                    CLIENT LAYER                          │
│  ┌──────────────────────────────────────────────────┐   │
│  │         React Frontend Application               │   │
│  │  - Home Dashboard                                │   │
│  │  - Class Timetable                               │   │
│  │  - Syllabus Management                           │   │
│  │  - Curriculum Overview                           │   │
│  │  - AI Assistant Interface                        │   │
│  └──────────────────────────────────────────────────┘   │
└───────────────────────┬─────────────────────────────────┘
                        │ HTTP/REST API
┌───────────────────────▼─────────────────────────────────┐
│                  APPLICATION LAYER                       │
│  ┌──────────────────────────────────────────────────┐   │
│  │         Node.js/Express Backend                  │   │
│  │  - RESTful API Routes                            │   │
│  │  - Business Logic Services                      │   │
│  │  - Request Validation                            │   │
│  │  - Error Handling                                │   │
│  └──────────────────────────────────────────────────┘   │
│  ┌──────────────────────────────────────────────────┐   │
│  │         External Service Integration              │   │
│  │  - Google Gemini API Client                      │   │
│  │  - API Key Management                            │   │
│  │  - Context Management                            │   │
│  └──────────────────────────────────────────────────┘   │
└───────────────────────┬─────────────────────────────────┘
```

## System Components

### Frontend Architecture

#### Technology Stack
- **React 18**: Component-based UI library
- **TypeScript**: Type-safe JavaScript
- **Vite**: Build tool and dev server
- **TailwindCSS**: Utility-first CSS framework
- **React Router DOM**: Client-side routing

#### Component Structure

```
frontend/src/
├── components/          # Reusable UI components
│   ├── Navbar.tsx
│   ├── Dashboard.tsx
│   └── ...
├── pages/               # Page components
│   ├── home.tsx
│   ├── ClassTimetable.tsx
│   ├── syllabus.tsx
│   ├── curriculum.tsx
│   └── chatbot.tsx
├── App.tsx              # Main application component
└── main.tsx             # Application entry point
```

#### Frontend Design Patterns

**Component-Based Architecture**:
- Reusable, composable components
- Props for data passing
- Hooks for state management
- Separation of presentation and logic

**State Management**:
- React hooks (useState, useEffect)
- Context API for global state (if needed)
- Local component state for UI state

**Routing**:
- React Router for navigation
- Route-based code splitting
- Protected routes (future enhancement)

### Backend Architecture

#### Technology Stack
- **Node.js**: JavaScript runtime
- **Express.js**: Web framework
- **TypeScript**: Type safety
- **CORS**: Cross-origin resource sharing

#### Backend Structure

```
backend/src/
├── routes/              # API route handlers
│   ├── chat.ts          # AI chat endpoints
│   └── ...
├── services/            # Business logic services
│   ├── gemini.ts        # Gemini API integration
│   └── ...
└── index.ts             # Server entry point
```

#### API Design

**RESTful Principles**:
- Resource-based URLs
- HTTP methods (GET, POST, PUT, DELETE)
- JSON request/response format
- Standard HTTP status codes

**Endpoint Examples**:
- `POST /api/chat` - AI chat interaction
  - Body: `{ messages: Array, syllabus?: string, rubric?: string }`
  - Response: `{ reply: string }` or `{ error: string }`
- `GET /api/health` - Server health status

### AI Integration Architecture

#### Google Gemini API Integration

```
┌──────────────┐
│   Frontend   │
│  (React)     │
└──────┬───────┘
       │ HTTP Request
       │ { messages, syllabus?, rubric? }
       ▼
┌──────────────┐
│   Backend    │
│  (Express)   │
└──────┬───────┘
       │ API Call
       │ with Context
       ▼
┌──────────────┐
│ Google       │
│ Gemini API   │
└──────┬───────┘
       │ AI Response
       ▼
┌──────────────┐
│   Backend    │
│  Processes   │
│  Response    │
└──────┬───────┘
       │ JSON Response
       ▼
┌──────────────┐
│   Frontend   │
│  Displays    │
└──────────────┘
```

#### Context Management

The AI assistant maintains context through:
- Conversation history tracking
- Syllabus content injection
- Rubric information inclusion
- User-specific preferences (future)

## Data Flow

### Request Flow Example: AI Chat

1. **User Input**: Faculty member types message in chat interface
2. **Frontend Processing**: React component captures input, formats request
3. **API Request**: POST request to `/api/chat` with:
   ```json
   {
     "messages": [...],
     "syllabus": "...",
     "rubric": "..."
   }
   ```
4. **Backend Processing**: Express route handler receives request
5. **Context Preparation**: Backend prepares context from syllabus/rubric
6. **Gemini API Call**: Backend calls Google Gemini API with context
7. **Response Processing**: Backend processes AI response
8. **Frontend Update**: React component receives and displays response

### Data Flow Diagram

```
User Action
    │
    ▼
Frontend Component
    │
    ▼
API Request (HTTP)
    │
    ▼
Express Route Handler
    │
    ├──► Validation
    ├──► Context Preparation
    └──► Gemini API Call
            │
            ▼
        AI Response
            │
            ▼
    Response Processing
            │
            ▼
    JSON Response (HTTP)
            │
            ▼
    Frontend Update
            │
            ▼
    User Sees Result
```

## Entity Relationship Model

### Conceptual Data Model

```
┌─────────────┐
│   Faculty   │
│   Member    │
└──────┬──────┘
       │
       │ teaches
       │
       ▼
┌─────────────┐      ┌─────────────┐
│   Course    │──────│  Syllabus   │
└──────┬──────┘      └─────────────┘
       │
       │ has
       │
       ▼
┌─────────────┐      ┌─────────────┐
│  Schedule   │──────│ Assignment  │
└─────────────┘      └─────────────┘
```

### Key Entities

**Faculty Member**
- User ID
- Name
- Email
- Department
- Courses taught

**Course**
- Course ID
- Course code
- Course name
- Credits
- Prerequisites

**Syllabus**
- Syllabus ID
- Course ID (FK)
- Content
- Learning objectives
- Grading breakdown
- Schedule

**Schedule/Timetable**
- Schedule ID
- Course ID (FK)
- Day of week
- Time
- Location
- Instructor

**Assignment**
- Assignment ID
- Course ID (FK)
- Title
- Description
- Due date
- Rubric

## Technology Decisions

### Why React?
- **Industry Standard**: Widely adopted, large ecosystem
- **Component Reusability**: Faster development
- **Performance**: Virtual DOM for efficient updates
- **TypeScript Support**: Excellent type safety

### Why Node.js/Express?
- **JavaScript Consistency**: Same language as frontend
- **Performance**: Non-blocking I/O
- **Ecosystem**: Large package ecosystem
- **Simplicity**: Easy to set up and maintain

### Why Google Gemini?
- **Advanced Capabilities**: State-of-the-art language model
- **Context Understanding**: Excellent at maintaining context
- **API Quality**: Well-documented, reliable API
- **Multimodal Support**: Future expansion possibilities

### Why TypeScript?
- **Type Safety**: Catch errors at compile time
- **Better IDE Support**: Autocomplete, refactoring
- **Self-Documenting**: Types serve as documentation
- **Maintainability**: Easier to maintain large codebases

## Security Architecture

### Security Measures

1. **API Key Protection**
   - Stored in environment variables
   - Never committed to repository
   - Server-side only access

2. **CORS Configuration**
   - Configured for specific origins
   - Prevents unauthorized access

3. **Input Validation**
   - Request validation on backend
   - Sanitization of user inputs
   - Error handling for malformed requests

4. **HTTPS** (Production)
   - Encrypted data transmission
   - Secure API communications

## Scalability Considerations

### Current Architecture Supports

- **Horizontal Scaling**: Stateless backend allows multiple instances
- **Caching**: Can implement caching layer for frequently accessed data
- **Database**: Ready for database integration when needed
- **CDN**: Static assets can be served via CDN

### Future Enhancements

- Database integration for persistent storage
- Caching layer (Redis) for performance
- Load balancing for high traffic
- Microservices architecture for complex features

