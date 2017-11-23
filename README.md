# tableExtractor
PHP - HTML Table Extractor

## Installation
Via composer:
```
composer require nanaksr/tableExtractor
```
## Configuration

## Usage
You can extract HTML table made easy
```
$source = @file_get_contents(__DIR__ . '/yout/file/path.htm', FILE_USE_INCLUDE_PATH);
if (!$source){
    echo "Data Source Not Found";
    exit();
}
$tblExt = new tableExtractor;
$tblExt->source = $source; 
$tblExt->anchor = 'Ticket';
$tblExt->stripTags = true;  
$tblExt->anchorWithin = true; 
$tblExt->headerRow = false; 
$ShowdataArray = $tblExt->extractTable();
```
