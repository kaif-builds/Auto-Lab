## Code Availability
The source code is kept private to preserve originality and prevent plagiarism. 
It can be shared upon request for academic or technical evaluation.
# 🔬 AutoLab: Practical Files, Perfected in Seconds.

> **"Stop formatting. Start submitting."**

AutoLab is a web-based productivity system designed to automate the entire practical file creation workflow. Users fill simple forms and generate a submission-ready PDF in one click.

It intelligently handles pasted content:
- Automatically formats raw text and messy input
- Preserves styling for pre-formatted content
- Supports rich text editing (bold, alignment, etc.)

## 🔗 Live Link
[auto-lab-final.vercel.app](https://auto-lab-final.vercel.app)



---

## 🚀 Why AutoLab?

Students spend more time fixing formatting than actually learning.

**Existing Problems:**

| Tool | Problem |
|---|---|
| Microsoft Word | Poor handling of code blocks and inconsistent formatting |
| Adobe Acrobat | Overkill for simple academic workflows |
| Manual Formatting | Time-consuming and error-prone |

**Solution:** AutoLab replaces generic tools with a purpose-built academic editor tailored for practical files.

---

## ✨ Key Features

### 🛠️ Smart Experiment Builder

A structured A4-based editing system designed for technical content.

- **Code-Aware Input** — Preserves indentation, spacing, and formatting from IDEs like VS Code
- **Image Layer System** — Drag, resize, and position images without breaking layout
- **Automatic Layout Enforcement** — Ensures consistent margins and formatting across all pages

### 📝 Guided Document Workflow

- **Cover Page Generator** — Generates standardized academic cover pages
- **Dynamic Indexing** — Automatically manages experiment listings
- **Full File Compilation** *(Upcoming)* — Merge all experiments into a single document

### ☁️ Cloud Sync & Data Handling

- **Auto-Save (Debounced)** — Saves user progress efficiently without excessive database writes
- **Session-Based Persistence** — Data is cleared after inactivity to maintain performance and privacy
- **Cross-Device Access** — Continue work seamlessly across devices

---

## 🧰 Tech Stack

**Frontend**
- React 18 + TypeScript + Tailwind CSS

**Backend & Services**
- Firebase Authentication
- Cloud Firestore (NoSQL Database)
- Firebase Storage (Image handling)

**Core Engine**
- jsPDF (Client-side PDF generation)
- Vite (Build tool)

---

## 🧠 System Architecture

AutoLab follows a **client-heavy architecture:**

```
User inputs data via UI
        ↓
React state manages document structure
        ↓
Local logic handles formatting and pagination
        ↓
Firestore stores data (if authenticated)
        ↓
jsPDF generates final output on the client
```

> **Key Design Decision:** All processing is handled client-side to ensure speed, scalability, and zero server cost for rendering.

---

## 📁 Project Structure

```
src/
├── components/        # Reusable UI components
├── pages/             # Main application views
├── hooks/             # Custom React hooks
├── utils/             # Helper functions (formatting, parsing)
├── services/          # Firebase & API integrations
├── lib/               # Core logic (pagination, PDF generation)
├── assets/            # Static resources
└── App.tsx            # Root component
```

---

## ⚙️ Core Functional Systems

**1. A4 Canvas Engine**
- Simulates real A4 pages using fixed dimensions
- Prevents overflow and enforces structure

**2. Auto Pagination System**
- Detects content overflow
- Splits content dynamically across pages
- Maintains formatting consistency

**3. Smart Paste Engine**
- Detects whether input is code or text
- Applies formatting rules accordingly
- Uses fallback logic if AI service is unavailable
- **AI-Powered Formatting** — If pasted content has little or no formatting, AutoLab sends it to an AI service to automatically clean, structure, and wrap it in proper tags before rendering

**4. PDF Rendering Engine**
- Converts structured state into PDF coordinates
- Generates documents entirely in the browser
- Ensures pixel-perfect output

---

## ⚡ Performance Optimizations

- Debounced auto-save to reduce database load
- Client-side image compression before upload
- Lazy rendering of pages
- Offline fallback for formatting

---

## 📈 Impact

- **Time Reduction:** ~30 minutes → under 5 minutes
- **Consistency:** Uniform formatting across submissions
- **Accessibility:** Works entirely in-browser, no paid tools required

---

## 🔮 Future Enhancements

- [ ] LaTeX support for mathematical equations
- [ ] Multi-university template system
- [ ] Real-time collaboration (multi-user editing)
- [ ] Plugin-based architecture for extensibility

---

## 👨‍💻 Developer

**Alkaif Gajdhar**
*Building systems that eliminate repetitive student workflows and improve productivity.*

[LinkedIn](https://www.linkedin.com/in/alkaif-gajdhar-b6033328b) | [GitHub](https://github.com/kaif-builds)

---

*© 2026 AutoLab. Designed for Medicaps University and beyond.*
