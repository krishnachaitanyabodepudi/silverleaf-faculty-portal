---
layout: default
title: Appendix
permalink: /appendix/
---

# Appendix

## Additional Resources

### Project Repository

- **GitHub Repository**: [https://github.com/krishnachaitanyabodepudi/silverleaf-faculty-portal](https://github.com/krishnachaitanyabodepudi/silverleaf-faculty-portal)

### Documentation

- **README.md**: Project overview and setup instructions
- **DEPLOYMENT_GUIDE.md**: Deployment and sharing instructions

## Video Demonstrations

### Project Demo Videos

*Note: Add your video links here. Example format:*

- **Full Project Demo**: [Video Link - Add your YouTube/Vimeo link here]
- **AI Assistant Demo**: [Video Link - Add your YouTube/Vimeo link here]
- **Dashboard Walkthrough**: [Video Link - Add your YouTube/Vimeo link here]
- **Syllabus Management Demo**: [Video Link - Add your YouTube/Vimeo link here]

### Video Embedding

To embed videos, you can use the following format in your markdown:

```html
<iframe width="560" height="315" src="YOUR_VIDEO_URL" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

## Images and Diagrams

### Architecture Diagrams

*Note: Add your architecture diagram images to `/assets/images/` and reference them here:*

- **Enterprise Architecture Diagram**: ![Enterprise Architecture](/assets/images/enterprise-architecture.png)
- **ER Diagram**: ![ER Diagram](/assets/images/er-diagram.png)
- **Data Flow Diagram**: ![Data Flow](/assets/images/data-flow.png)

### Screenshots

*Note: Add your application screenshots to `/assets/images/` and reference them here:*

- **Home Dashboard**: ![Dashboard](/assets/images/dashboard.png)
- **AI Assistant Interface**: ![AI Chat](/assets/images/ai-chat.png)
- **Syllabus Management**: ![Syllabus](/assets/images/syllabus.png)
- **Class Timetable**: ![Timetable](/assets/images/timetable.png)

## API Documentation

### Endpoints

#### POST /api/chat

Send messages to AI assistant.

**Request Body**:
```json
{
  "messages": [
    {
      "role": "user",
      "content": "Help me create a lesson plan for data structures"
    }
  ],
  "syllabus": "Optional syllabus content for context",
  "rubric": "Optional rubric content for context"
}
```

**Response**:
```json
{
  "reply": "AI-generated response text"
}
```

**Error Response**:
```json
{
  "error": "Error message"
}
```

#### GET /api/health

Server health status check.

**Response**:
```json
{
  "status": "healthy"
}
```

## Technology Versions

### Frontend Dependencies

- React: ^18
- TypeScript: 5.9.3
- Vite: (via build tool)
- TailwindCSS: ^3.3.0
- React Router DOM: (latest)
- Lucide React: (latest)

### Backend Dependencies

- Node.js: v18 or higher
- Express: (via npm)
- TypeScript: 5.9.3
- @google/generative-ai: ^0.2.1
- CORS: (via npm)

## Installation Instructions

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn

### Setup Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/krishnachaitanyabodepudi/silverleaf-faculty-portal.git
   cd silverleaf-faculty-portal
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   - Create `.env.local` file
   - Add `GEMINI_API_KEY=your_api_key_here`

4. **Start development servers**
   ```bash
   npm run dev
   ```

5. **Access the application**
   - Frontend: http://localhost:5173
   - Backend: http://localhost:3001

## Deployment Options

### Option 1: Vercel

1. Install Vercel CLI: `npm install -g vercel`
2. Run: `vercel`
3. Follow prompts
4. Set environment variables in Vercel dashboard

### Option 2: Netlify

1. Build the project: `npm run build`
2. Upload `.next` folder to Netlify
3. Set environment variables in site settings

### Option 3: Railway

1. Connect GitHub repository
2. Add environment variable: `GEMINI_API_KEY`
3. Deploy automatically

## Project Statistics

### Code Metrics

- **Total Files**: (Update with actual count)
- **Lines of Code**: (Update with actual count)
- **Components**: (Update with actual count)
- **API Endpoints**: 2 (chat, health)

### Development Timeline

- **Project Start**: (Add date)
- **Project Completion**: (Add date)
- **Total Development Time**: (Add duration)

## Acknowledgments

### Technologies Used

- React Team for the excellent framework
- Google for Gemini API
- Vite team for the build tool
- TailwindCSS team for the CSS framework
- All open-source contributors

### Resources

- React Documentation: https://react.dev
- Google Gemini API: https://ai.google.dev
- Vite Documentation: https://vitejs.dev
- TailwindCSS Documentation: https://tailwindcss.com

## Contact Information

### Project Maintainer

- **GitHub**: [krishnachaitanyabodepudi](https://github.com/krishnachaitanyabodepudi)
- **Repository**: [silverleaf-faculty-portal](https://github.com/krishnachaitanyabodepudi/silverleaf-faculty-portal)

### Support

For support and questions, please contact the Silverleaf University IT department or open an issue on GitHub.

## License

This project is licensed under the MIT License.

---

*This appendix contains additional resources, documentation, and supplementary information for the Silverleaf University Faculty Portal project.*

