# HTML Extractor
PHP - HTML Table Extractor

## Installation
Via composer:
```
composer require nanaksr/htmlextractor
```
## Quick Start and Example
```
require __DIR__ . '/vendor/autoload.php';

use \nanaksr\htmlextractor;

$source = @file_get_contents(__DIR__ . '/yout/file/path.htm', FILE_USE_INCLUDE_PATH);
if (!$source){
    echo "Data Source Not Found";
    exit();
}
$tblExt = new htmlextractor;
$tblExt->source = $source; 
$tblExt->anchor = 'id';
$tblExt->stripTags = true;  
$tblExt->anchorWithin = true; 
$tblExt->headerRow = false; 
$ShowdataArray = $tblExt->extractTable();
```
