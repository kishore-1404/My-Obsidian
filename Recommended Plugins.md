# Recommended Obsidian Plugins

This note contains a list of recommended Obsidian plugins that can enhance your placement preparation and internship tracking experience.

## Core Plugins (Built-in)
These are built into Obsidian and just need to be enabled:

1. **Daily Notes** - Already in use for your daily notes
2. **Templates** - Already in use for your templates
3. **Outgoing Links** - See what notes link to the current note
4. **Tag Pane** - View and navigate all your tags
5. **Graph View** - Visualize connections between notes
6. **Backlinks** - See what notes link to the current note
7. **Search** - Advanced search capabilities
8. **Starred** - Star your most important notes for quick access
9. **Quick Switcher** - Quickly jump between notes (Ctrl+O)
10. **Page Preview** - Hover over links to preview their content

## Community Plugins (Need to be installed)

### Essential for Your Workflow

1. **DataView** - Create dynamic lists and tables from your notes
   - Use case: Track progress across different notes, create dashboards
   - Example query: Show all DSA problems solved this week

2. **Kanban** - Create kanban boards
   - Use case: Visualize your placement preparation progress
   - Example: Create a board for DSA topics (To Learn, Learning, Learned)

3. **Calendar** - Calendar view of your daily notes
   - Use case: Navigate daily notes and see progress at a glance
   - Benefits: Visual representation of your work over time

4. **Templater** - Advanced templating (more powerful than built-in Templates)
   - Use case: Create more dynamic templates with complex variables
   - Already seems to be in use in your vault

### For DSA Practice

5. **Code Block Enhancer** - Better code blocks with line numbers, copy button
   - Use case: Improve how code appears in your DSA notes
   - Benefits: Better readability and organization of code

6. **Syntax Highlight** - Improved syntax highlighting for code
   - Use case: Make your code more readable in DSA notes
   - Supports many programming languages

7. **Excalidraw** - Draw diagrams and visualizations
   - Use case: Visualize algorithms and data structures
   - Example: Draw a tree traversal or graph algorithm

### For Organization and Productivity

8. **Tracker** - Track habits and daily activities
   - Use case: Track your daily DSA practice and study habits
   - View stats and streaks for motivation

9. **Progress Bar** - Visualize progress toward goals
   - Use case: Track completion of DSA topics or aptitude questions
   - Example: Show "50% of DSA topics covered"

10. **Tag Wrangler** - Better management of tags
    - Use case: Rename, merge, and organize your tags
    - Benefits: Keep your tagging system clean and organized

11. **Obsidian Tasks** - Advanced task management
    - Use case: Track tasks across your vault with due dates
    - Filter tasks by status, due date, etc.

12. **Mind Map** - Create mind maps from your notes
    - Use case: Visualize concepts and connections
    - Example: Create a mind map of data structure relationships

### For Better Note-Taking

13. **Advanced Tables** - Improved table editing
    - Use case: Create better-formatted tables in your notes
    - Features: Table formatting, formulas, sorting

14. **Outliner** - Better outline and list management
    - Use case: Create structured outlines for complex topics
    - Features: Collapsible lists, better indentation

15. **Admonition** - Create callout boxes in your notes
    - Use case: Highlight important information or warnings
    - Example: Create a warning box for common mistakes in a topic

### For Spaced Repetition

16. **Spaced Repetition** - Create flashcards from your notes
    - Use case: Review DSA concepts and aptitude formulas
    - Features: Integrated spaced repetition system

17. **Review** - Schedule notes for review
    - Use case: Implement spaced repetition for learning
    - Features: Set review intervals for notes

## Installation Instructions

1. Open Obsidian settings
2. Go to "Community plugins"
3. Turn off "Safe mode" if it's enabled
4. Click "Browse" to see available plugins
5. Search for the plugin you want
6. Click "Install", then "Enable"

## Example DataView Queries

### Show all DSA problems solved
```dataview
TABLE
  file.cday as "Date Created",
  tags as "Tags"
FROM #dsa
WHERE contains(file.name, "DSA-")
SORT file.cday DESC
```

### Track progress by difficulty
```dataview
TABLE length(rows) as "Count"
FROM #dsa
WHERE contains(file.name, "DSA-")
GROUP BY choice(contains(tags, "#easy"), "Easy", choice(contains(tags, "#medium"), "Medium", "Hard"))
```

### Show upcoming placement tasks
```dataview
TASK
FROM #placement
WHERE !completed
SORT due ASC
```
