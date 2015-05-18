# data-ilt-treemap


To use this:

- you need to download all the files and directories in the repo locally
- point your browswer at <localdir>/<various>.html using the browser file command

  - index.html is a "zoomable tree map" of all (*) database offerings in categories.
    You can zoom in and out of the hierarchy, and you can change the criteria 
    from "size" (which is a a ranking of "popularity" taken from db-engines.com),
    and "count". 
  - index2.html is a "sunburst" visualization of all (*) the database categories 
    and offerings. NOTE: today there are no labels and no key. Should be enhances
    to allow you to get information on an offering by "hovering" over it. 
  - tax-indended.tree.html is an "indented treemap" of the full taxonomy for the 
    "Data" landscape (broader than just databases, includes storage software, 
    BI/EDW, data processing, etc).
  - tax-dndTree.html is a visualization of all (*) the database categories and
    offerings as a "tree" that supports click to zoom/collapse portions of the 
    tree, and supports "drag" to center/move the tree, etc. 

(*) ALL is actually a subset. I has some issues with JSON related errors (which 
    can probably be fixed) that implied there were "too many array entries", 
    so "ALL" is really "ALL entries with DB-Engins.com ranking >= .1 (essentially
    weeding out a good number of "stragglers"). These visualizations should
    really support "cutoff criteria", etc. 

NOTE: this will ONLY work with Firefox and Safari, there is a "cross platform
security" issue with Google Chrome (at least on OS-X, it may work on Linux).


