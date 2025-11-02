🌟 Lumina
Your thoughts, beautifully kept

A privacy-first, offline-capable note-taking sanctuary for solo thinkers. Zero login, zero hassle, 100% yours.

✨ What Makes Lumina Special?
🔒 Radical Privacy
All your notes stay in your browser's IndexedDB. No servers, no tracking, no account required.

📱 Fully Responsive
Beautiful on every device - phone, tablet, or desktop. Touch-optimized with WCAG-compliant accessibility.

🎨 Luminous Design
Glass-morphism aesthetic with soft glows and poetic interactions. Light and dark themes with custom accent colors.

📝 Rich Text Editing
Powered by Tiptap with Markdown support, to-do lists, and auto-save.

📄 File Attachments
Upload and view PDF documents and PowerPoint presentations directly in your notes.

🤖 AI Assistant (Optional)
DeepSeek-powered assistant to summarize or improve your notes (requires API key).

🌬️ Breathe Mode
Press ESC for a guided breathing overlay to refocus your mind.

📦 Multi-Format Export
Export notes as TXT, HTML, PDF, DOCX, or XLSX - your data, your format.

🎭 Typography Heaven
Choose from 12 carefully curated Google Fonts across 6 categories, with 17 font size options (8px-72px).

🚀 Quick Start
Prerequisites
Node.js 18+
npm or yarn
Installation
# Clone the repository
git clone <your-repo-url>
# Install dependencies
npm install
# Start the development server
npm run dev

The app will be available at http://localhost:5000

Environment Variables
For AI features, add your DeepSeek API key to .env:

DEEPSEEK_API_KEY=your_api_key_here
SESSION_SECRET=your_session_secret

📖 Features in Detail
📝 Note Taking
Rich text editor with Tiptap
Markdown support for quick formatting
To-do lists with interactive checkboxes
Auto-save every change to IndexedDB
Automatic title extraction from first line
📎 File Management
PDF viewer with page navigation (powered by PDF.js)
PowerPoint upload and download
Files stored as blobs in IndexedDB per note
No file size limits (within browser storage constraints)
🎨 Customization
Theme modes: Light, Dark, or System auto-switching
Custom accent colors: Choose your brand color
Font selection: 12 Google Fonts across 6 categories:
Sans-serif: Inter, Roboto, Open Sans, Lato, Montserrat, Poppins, Source Sans 3
Serif: Cormorant Garamond, Playfair Display, Lora, Merriweather
Monospace: JetBrains Mono
Font sizes: 17 options from 8px to 72px (Microsoft Office-level precision)
📤 Export & Share
Export notes in multiple formats:

Plain Text (.txt) - Clean text extraction
HTML Document (.html) - Beautiful self-contained pages
PDF Document (.pdf) - Professional formatted PDFs
Word Document (.docx) - Editable DOCX files
Excel Spreadsheet (.xlsx) - Table or text sheets
All exports include a branded footer: "Exported from Lumina"

🧘 Wellbeing
Breathe Mode (ESC key) - Guided breathing overlay
Distraction-free writing - Calm, focused environment
Poetic interactions - Empty state: "Light begins with a single thought"
🤖 AI Assistant (Optional)
Powered by DeepSeek API
Summarize, improve, or transform your notes
Secure backend proxy (API key never exposed to frontend)
Input validation and rate limiting
📱 Responsive Design
Mobile (< 768px)
Slide-in sidebar with hamburger menu
Touch-optimized 44x44px buttons
Essential features always visible
Responsive padding (p-3)
Tablet (768-1023px)
Slide-in sidebar drawer
Progressive UI with more controls
WCAG-compliant touch targets
Optimized for iPad and Android tablets
Desktop (≥ 1024px)
Permanent sidebar (280px)
All controls visible
Font selectors and advanced features
Generous spacing (p-6)
🏗️ Technical Architecture
Frontend
React + TypeScript - Type-safe component development
Wouter - Lightweight routing
TanStack Query - State management and caching
Tiptap - Rich text editing
Tailwind CSS - Utility-first styling
Shadcn/ui - Beautiful component library
IndexedDB - Client-side storage
Backend
Express.js - Minimal server for AI proxy
CORS and JSON middleware
Environment variable handling
Security-first design
External Libraries (CDN)
PDF.js - PDF rendering
html2pdf.js - PDF export
docx - Word document generation
xlsx - Excel spreadsheet creation
Mammoth.js - PowerPoint conversion
🎨 Design Philosophy
Light as Metaphor
Notes appear as glowing "light panels" with glass-morphism. Every interaction feels luminous - soft glows, gentle transitions, breathing space.

No Harsh Edges
Border radius of 12-16px consistently
Subtle shadows and inner glows instead of hard borders
Smooth transitions and animations
Typography as Mood
Carefully selected fonts reflect different emotional contexts:

Clarity: Inter, Roboto, Open Sans
Soul: Cormorant Garamond, Playfair Display
Precision: JetBrains Mono
Color System
Light mode: Pure white background with subtle grays
Dark mode: Deep navy background with soft contrast
Accent: Customizable (default: indigo #6366f1)
Glow effects: Dynamic based on accent color
🗄️ Data Storage
Note Schema
interface Note {
  id: string;
  content: string; // HTML from Tiptap
  title: string; // Auto-extracted
  updatedAt: number; // Timestamp
  pdf?: Blob; // Optional PDF attachment
  pptx?: Blob; // Optional PowerPoint
}

User Settings (localStorage)
interface UserSettings {
  theme: 'light' | 'dark' | 'system';
  accentColor: string;
  fontFamily: string;
  fontSize: number; // 8px to 72px
}

🔒 Security Features
Privacy-First
✅ No analytics or tracking
✅ No server-side data storage
✅ No login or authentication required
✅ All data stays in your browser
XSS Protection
✅ Sanitized file viewer output
✅ No dangerouslySetInnerHTML
✅ Sanitized error messages
✅ Input validation on all endpoints
API Security
✅ Rate limiting on AI endpoint
✅ 10k character prompt limit
✅ Model whitelist validation
✅ Stack trace prevention in errors
🛠️ Development
Project Structure
lumina/
├── client/
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── pages/          # Page components
│   │   ├── hooks/          # Custom hooks
│   │   ├── lib/            # Utilities
│   │   └── App.tsx         # Root component
├── server/
│   ├── ai-proxy.ts         # DeepSeek API proxy
│   ├── routes.ts           # API routes
│   └── index.ts            # Server entry
├── shared/
│   └── schema.ts           # Shared types
└── package.json

Key Commands
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build

Environment Setup
Copy .env.example to .env
Add your DeepSeek API key (optional)
Generate a session secret
Run npm run dev
🌐 Browser Support
✅ Chrome 90+
✅ Firefox 88+
✅ Safari 14+
✅ Edge 90+
Required Features:

IndexedDB support
ES6+ JavaScript
CSS Grid and Flexbox
📄 License
MIT License - See LICENSE file for details

Lumina is 100% open-source and free forever. No paywalls, no premium tiers, no restrictions.

🙏 Acknowledgments
Built With
Tiptap - Rich text editor
Shadcn/ui - Component library
Tailwind CSS - Styling
TanStack Query - State management
PDF.js - PDF rendering
DeepSeek - AI assistance
Design Inspiration
Glass-morphism, modern minimalism, and the beauty of focused writing.

🚀 Roadmap
 Night Sky Archive (trash/restore deleted notes)
 Version history tracking
 Offline-first PWA support
 End-to-end encryption option
 More AI actions (translate, expand, etc.)
 Custom themes builder
 Keyboard shortcuts panel
💬 Support
Having issues? Found a bug?

Check existing issues on GitHub
Create a new issue with reproduction steps
Include your browser version and OS
🌟 Star This Project
If Lumina helps you keep your thoughts beautifully organized, consider giving it a ⭐ on GitHub!

Made with 💙 for solo thinkers who value privacy, beauty, and focus.

Light begins with a single thought.
