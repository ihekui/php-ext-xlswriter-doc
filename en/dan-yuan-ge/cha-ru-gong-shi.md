# Insert formula

### **Function Prototype**

```php
insertFormula(int $row, int $column, string $formula)
```

#### **int $row**

> cell row

#### **int $column**

> cell column

#### **string $formula**

> formula

###example

```php
$excel = new \Vtiful\Kernel\Excel($config);

$freeFile = $excel->fileName("free.xlsx")
     ->header(['name', 'money']);

for($index = 1; $index < 10; $index++) {
     $textFile->insertText($index, 0, 'viest');
     $textFile->insertText($index, 1, 10);
}

$textFile->insertText(12, 0, "Total");
$textFile->insertFormula(12, 1, '=SUM(B2:B11)');

$freeFile->output();
```