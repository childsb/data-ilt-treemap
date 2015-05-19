# data-ilt-treemap

To use this:

- you need to download all the files and directories in the repo locally
- point your browswer at <localdir>/<various>.html using the browser file command

File (.html)		Visualization Type			Of
===================================================================================
zoomable-treemap	Rectangular treemap; select; zoom	All databases, *
zoomable-sunburst	"sunburst" arrangement; select; zoom    All databases, *, **
dndTree			Clickable/dragable tree; click+/-	All databases, *
bubble			bubble area chart			All databases, *

radial-tree		Radial Tree arrangement			All databases
cluster-dendrogram	Tree with leaves "aligned"		All databases

tax-indented-tree       "Clickable indented tree"; click+/-	All categories

Key: 
===================================================================================
select 		Allows user to "select" a criteria (eg: size or count) to visualize
                on; implemented as a mutually exclusive selection criteria
click +/-	Allows user to click an object (usually to expand/collapse detail
                underneath that object)
zoom  		Allows user to "zoom" in on a point of reference by clicking it (and 
                zoom back out by clicking elsewhere).

All database    A full list of all database offering (relational and non-relational)
                including more obscure offerings and offering types (no filtering).

All categories  A list of all the categories, including the non-database categories, 
                not all the entries.

*               These visualizaitons should support some sort of "cutoff" criteria,
                to allow user to filter.
**              This visualization currently has no labels; need to implement labels
                or some sort of mouse-over/hover to allow user to indentify details.

NOTE: this will ONLY work with Firefox and Safari, there is a "cross platform
security" issue with Google Chrome (at least on OS-X, it may work on Linux).


