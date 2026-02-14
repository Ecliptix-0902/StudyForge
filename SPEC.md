# StudyForge - Core Task + XP System Specification

## Project Overview
- **Project Name**: StudyForge
- **Type**: Gamified Task Management Web App
- **Core Functionality**: A task management app that rewards completed tasks with XP and leveling up
- **Target Users**: Students who want to gamify their homework/study tasks

---

## UI/UX Specification

### Layout Structure

**Page Sections (top to bottom):**
1. Header Section - Title and subtitle
2. Input Section - Task input field and add button
3. Task List Section - Scrollable list of task cards
4. Progress Section - XP display, level display, and XP bar

**Responsive Breakpoints:**
- Mobile: < 600px (full width, stacked)
- Desktop: >= 600px (centered, max-width 600px)

### Visual Design

**Color Palette:**
- Background: `#0f0f1a` (deep dark purple-black)
- Card Background: `#1a1a2e` (slightly lighter dark)
- Card Hover: `#252542` (lighter on hover)
- Primary Accent: `#6366f1` (indigo/purple)
- Primary Hover: `#818cf8` (lighter purple)
- Text Primary: `#ffffff` (white)
- Text Secondary: `#9ca3af` (muted grey)
- XP Bar Background: `#374151` (dark grey)
- XP Bar Fill: Linear gradient from `#6366f1` to `#a855f7` (purple gradient)
- Success/Glow: `rgba(99, 102, 241, 0.3)` (purple glow)

**Typography:**
- Font Family: `'Outfit', sans-serif` (Google Fonts)
- Title: 48px, bold, letter-spacing: 4px
- Subtitle: 16px, weight 400, color secondary
- Task Text: 18px, weight 500
- XP/Level Text: 20px, weight 600

**Spacing System:**
- Container padding: 24px
- Card padding: 16px 20px
- Gap between elements: 16px
- Border radius (cards): 12px
- Border radius (buttons): 8px
- Border radius (input): 8px

### Components

**1. Header**
- Centered title "STUDYFORGE" with letter spacing
- Subtitle "Turn homework into XP." below

**2. Input Section**
- Flexbox row with gap 12px
- Input field: dark grey bg, white text, placeholder "Enter a task..."
- Button: purple accent, white text "Add Task", pointer cursor

**3. Task Card**
- Dark card with subtle border
- Cursor: pointer
- Hover: subtle glow effect, slight scale transform
- Transition: 0.2s ease

**4. Progress Section**
- XP and Level displayed in a row
- XP bar below with smooth width transition (0.3s ease)
- Bar fills based on current XP / 100

---

## Functionality Specification

### Core Features

**1. Add Task**
- User types task in input field
- Click "Add Task" button or press Enter
- If input is empty: do nothing
- Create new task card and add to list
- Clear input field after adding

**2. Complete Task**
- Click on any task card to complete it
- Award 10 XP instantly
- Remove task from list with smooth transition

**3. XP System**
- Starting XP: 0
- XP per task: 10
- XP needed per level: 100

**4. Level System**
- Starting Level: 1
- When XP >= 100:
  - Increase level by 1
  - Subtract 100 from XP (not reset to 0)
  - Update level display

**5. XP Bar**
- Width = (currentXP / 100) * 100%
- Smooth animation on update
- Gradient fill from purple to violet

### User Interactions
- Input: type task → click Add or press Enter
- Task: click to complete → XP increases → task removed

### Edge Cases
- Empty input: ignore add action
- Very long task text: truncate with ellipsis
- Level up at exactly 100 XP: level up, XP becomes 0

---

## Acceptance Criteria

1. ✓ Title "STUDYFORGE" displays centered at top
2. ✓ Subtitle "Turn homework into XP." displays below title
3. ✓ Input field accepts text with placeholder "Enter a task..."
4. ✓ "Add Task" button adds task to list when clicked
5. ✓ Pressing Enter in input also adds task
6. ✓ Empty input does not create task
7. ✓ Tasks display as dark cards in a list
8. ✓ Clicking a task completes it and removes from list
9. ✓ Completing a task adds 10 XP
10. ✓ XP display updates instantly
11. ✓ Level increases by 1 when XP reaches 100
12. ✓ XP resets to (XP - 100) after level up
13. ✓ XP bar fills proportionally to XP / 100
14. ✓ XP bar animates smoothly on update
15. ✓ No page refresh occurs
16. ✓ No alerts or popups appear
17. ✓ Dark theme throughout
18. ✓ Smooth hover effects on tasks and buttons

---

## File Structure
```
/Users/rannveersingh/Desktop/StudyForge/
└── index.html (single file with embedded CSS and JS)
```

