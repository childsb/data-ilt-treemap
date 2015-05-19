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


Directories:
===================================================================================
. (root)	Contains .html files
./js  		Contains JavaScript (.js) files
./json		Contains JSON (.json) data files
./css		Contains CSS style sheets

JSON Data Files
===================================================================================

raw-data.csv	Raw data from Google Spreadsheet (); downloaded as a .csv file
convertcsv.json raw-data-csv file converted to JSON using web service @ 
                http://www.convertcsv.com/csv-to-json.htm

database-taxonomy-template
                "template file", hold sturcture for the database-taxonomy

database-taxonomy-all.json
                All database offerings, all fields (including "website", "details"
                and "type"). 

database-taxonomy-size-10-plus.json
                All database offerings, but only "name" and "size" fields, and
                only offerings with "size" >= 10. (weeds out the stragglers mannually)
database-taxonomy-size-all.json
                All database offerings, but only "name" and "size" fields, for all
                offerings regardless of size (so includes the stragglers).

content-store.json
data-taxonomy.json
document-store.json
event-store.json
graph-dbms.json
key-value-store.json
multi-model.json
multivalue-dbms.json
native-xml-dbms.json
navigational-dbms.json
object-oriented-dbms.json
rdf-store.json
relational-dbms.json
search-engine.json
wide-column-store.json
                 JSON files for individual database categories (e.g. relational-dbms.json
                 for all offerings where "type" = "Relational DBMS"). These files are 
                 effectively substitued for the "--DUMMY NAME--" entry in the template file
                 (json/database-taxonomy-template). 
