<< [[<% moment(tp.file.title, 'YYYY-MM-DD').subtract(1, 'days').format('YYYY-MM-DD') %>|Yesterday]] | [[<% moment(tp.file.title, 'YYYY-MM-DD').add(1, 'days').format('YYYY-MM-DD') %>|Tomorrow]] >>


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
