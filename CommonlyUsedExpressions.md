### Replace

Allows you to replace any pattern with another pattern

replace(value, 'pattern_in_metadata', 'new_pattern_to_insert')

e.g. replace(value, 'Tennessee', '(Tenn.)')


### Numbers to String

value.floor().toString()

Use when ISBNs or other long numbers (like identifiers) get converted to float numbers unintentionally and won’t transform correctly


### Fixing Dates

value.toDate('MM/yy/dd','MMM-yy-dd').toString('yyyy-MM-dd')

Goes from machine readable (aka yyyy-MM-ddT00:00:00Z) to edtf (yyyy-MM-dd)


### Cell Cross

Adding a column from a separate project to your existing project. This allows you to add a column without having to export to Excel and lose your edit history.

From Gretchen Geugen:
[https://github.com/dpla/Metadata-Analysis-Workshop/blob/master/OpenRefine.md](https://github.com/dpla/Metadata-Analysis-Workshop/blob/master/OpenRefine.md)
From OpenRefine: 
[https://github.com/OpenRefine/OpenRefine/wiki/GREL-Other-Functions](https://github.com/OpenRefine/OpenRefine/wiki/GREL-Other-Functions) 

### Additional Instructions

String Functions - [https://github.com/OpenRefine/OpenRefine/wiki/GREL-String-Functions](https://github.com/OpenRefine/OpenRefine/wiki/GREL-String-Functions)


