

## TODO
- [X] draw series
    - when clicked on checkbox in legend-item, it draws colorful series
        - "" in yVar makes parseFloat(yVra) become 0 or NaN.
- [X] sort function
    - when clicking on sort icons, sort legend items by name or score
        - problem: casting number and string, NaN in numbers
        - resolution: change sort function
- [X] add bold
    - when click on label, if drawn, make legend item and series bold
        - make all non-bolds passive
        - when removed, make passives active
- [X] add horizontal annotation
- [X] add mouse-over on series 
    - when mouse over, both legend item and line become bold
- [X] legendCheckboxHandler can be done when creating legend item from template
- [X] move all event handlers to inline in html
    - each template element should have the event handlers
    - why? then we do not need to worry about if the element populated when deploying the event handler
- [X] change sort function to have sort(by, direction) and make it inline for readability
- [X] git commit to invisement and tmo
- [X] change of y-axis to logarithm
    - working data: db-ranking
    - problems: y-axis range too wide, double-click: error
    - added manual entries for x and y range
    - changed double-click to closest row
- [X] draw upon reading query parameters
    - setup easel
    - read params and do actions
- [X] create view mode that does not have the header
- [X] add sort by importance (bold, check, uncheck)
- [X] #BUG: labels do not have color
- [X] add sorts to actions 
- [ ] when changing y-var it draws the same graph
    - write a function get snapshot to get bolds, selected
- [ ] add title, x label, y label

- [ ] reading from url
- [ ] read from url with shortening url for datasets
- [ ] use it for tmo operational chart
- [X] upload it for public view
- [ ] add tooltip (title) to mouse on points
- [ ] dialog to create actions
- [ ] rewrite legend.filter function
    - get condition and then apply to list of nodes
    - right now, for each element, it evaluates the condition



## Markdown editor

## summary table

## reference cell and data in markdown

## table editor (excel in markdow)

## add query parameter ui

# how to use
parameters get fetch from url's query parameters
- example: url=../data/db-ranking.csv
    &xVar=month&yVar=value&slicer=db-name&y-log=true&y-min=0.1
    &filter=:top35&selectAll&bold=Google BigQuery,Cassandra&mode=view&filter=&sort
- filter (defined in legend.filter()) specials starts with :
    - :bold, :top10, :bottom30, :check, :uncheck, w:bold, washi
- actions (in params): defined in easel.actions()
    - selectAll, selectNone, sort, sort=-label, filter=whatever, mode=view, bold=this,that, select=this,that, deselect=this,that


