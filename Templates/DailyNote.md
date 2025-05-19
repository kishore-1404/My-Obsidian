---
date: <% tp.file.title %>
week: <% moment(tp.file.title, 'YYYY-MM-DD').format('W') %>
---

# <% moment(tp.file.title, 'YYYY-MM-DD').format('dddd, MMMM D, YYYY') %>

<< [[<% moment(tp.file.title, 'YYYY-MM-DD').subtract(1, 'days').format('YYYY-MM-DD') %>|Yesterday]] | [[<% moment(tp.file.title, 'YYYY-MM-DD').add(1, 'days').format('YYYY-MM-DD') %>|Tomorrow]] >>

## 📋 Task Management

> [!multi-column]
> 
> > [!todo]+ Task Due Today
> > ```tasks
> > not done
> > due <% tp.file.title %>
> > hide due date
> > ```
> 
> > [!danger]+ Overdue Tasks
> > ```tasks
> > not done
> > due before <% tp.file.title %>
> > hide due date
> > ```

> [!multi-column]
> 
> > [!success]+ Completed Tasks
> > ```tasks
> > done <% tp.file.title %>
> > ```
> 
> > [!abstract]+ Task Due Later
> > ```tasks
> > not done
> > due after <% tp.file.title %>
> > ```

## 💻 DSA Practice
- [ ] [[Notes/SDE/DSA/DSA-<% tp.file.title %>.md|Today's DSA Problems]] 📅 <% tp.file.title %>

## 🧩 Aptitude & Puzzle Practice
> [!note]- Weekly Goal
> Solve at least 5 aptitude questions and 2 puzzles per week

- [ ] [[Notes/SDE/Aptitude/Aptitude-<% tp.file.title %>.md|Today's Aptitude & Puzzles]] 📅 <% tp.file.title %>

## 🏢 Summer Internship
- [ ] [[Notes/Internship/Internship-<% tp.file.title %>.md|Today's Internship Work]] 📅 <% tp.file.title %>

## 📚 Placement Preparation
- [ ] [[Notes/SDE/Placement/Placement-<% tp.file.title %>.md|Today's Placement Prep]] 📅 <% tp.file.title %>

## 📝 Reflection
- **Accomplishments:**
	- 

- **Areas for Improvement:**
	- 

- **Plan for Tomorrow:**
	- 

## 💡 Ideas & Notes
- 
