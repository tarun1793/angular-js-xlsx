# mf-angular-js-xlsx
An angular directive to read XLSX / XLSM / XLSB / XLS / SpreadsheetML (Excel Spreadsheet) [https://github.com/SheetJS/js-xlsx](https://github.com/SheetJS/js-xlsx)

# Installation

```
  # Bower
  bower install mf-angular-js-xlsx
  # NPM
  npm install mf-angular-js-xlsx
```

# Use

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Angular Js XLS</title>
</head>
<body ng-app="MyApp">
  <div ng-controller="myController">
    <js-xls onread="read" onerror="error"></js-xls>
  </div>

  <script type="text/javascript" src="angular.min.js"></script>
  <script type="text/javascript" src="xlsx.core.min.js"></script>
  <script type="text/javascript" src="angular-js-xlsx.js"></script>
  <script type="text/javascript">
    angular.module('MyApp', ['angular-js-xlsx'])
    .controller('myController', function($scope) {
      $scope.read = function (workbook) {
        /* DO SOMETHING WITH workbook HERE */
        console.log(workbook);
        console.log(workbook.fileProps)
      }

      $scope.error = function (e) {
        /* DO SOMETHING WHEN ERROR IS THROWN */
        console.log(e);
      }
    });
  </script>
</body>
</html>
```
