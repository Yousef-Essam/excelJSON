# excelJSON
A simple package based on the xlsx package to covert from Spreadsheet data to JSON and vice versa

## Installation
`npm install excelJSON`

## Usage
### Importing the package
`const excelJSON = require('excelJSON')`
### To convert Spreadsheet data to JSON data

`let xlsxFile = await fs.readFile('file.xlsx');`   
`let convertedJSON = excelJSON.XLSXToJson(xlsxFile, 'Sheet Name')`  
`// The second parameter is required and it represents the sheet name inside the Spreadsheet file.`
### To convert JSON data to Spreadsheet data

`let jsonFile = JSON.parse(await fs.readFile('file.json', 'utf-8'));`
`let convertedXLSX = excelJSON.jsonToXLSX(jsonFile, 'Sheet Name')`  
`// The second parameter is required and it represents the sheet name inside the xlsx file.`  
`// This function produces an excel file with only one sheet whose name is provided using the second parameter`
