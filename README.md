# catalogo

front end for data sets on D4Maia datalake

## Current version 

Current version is setup to run both locally (disconnected from the net) / @baze.cm-maia.pt with minor changes at the headers, where jquery is loaded.


This front end should be invoked with the following parameters:
- e0=<name> - name of the dataset to be described
- chart={on|off} - selecting to display / no display of the chart
- lista={sigla|\*} - selecting if the console lists the short name ("sigla") or full name of the series 
- x=<keypass> - value of a keypass that allows editing the metadata 

full url examples:
https://baze.cm-maia.pt/BaZe/catalogo2.htm?chart=off&x=<keypass>&e0=0008231
https://baze.cm-maia.pt/BaZe/catalogo2.htm?chart=off&x=<keypass>&e0=NInstCult

## Main tasks

The page starts (onload=....) by lecat()

### lecat()
- settting layout dimensions
- parsing the current url and extracts charting, keypass, lista () and (short) name of the series to be accessed
- composes url to call endpoint http(...)/api/api4scat.php - api catalog of available series
- $getjson (JQuery) to get and parse end endpoint response
- the response is parsed and the left lateral menu of the console is buil


= The end