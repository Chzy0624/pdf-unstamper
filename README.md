# pdf-unstamper
Remove text stamps of **any font**, **any encoding** and **any language** with pdf-unstamper now!

Powered by [Apache PDFBox®](https://pdfbox.apache.org/).

## Effect
<table>
<thead>
<tr>
<th>Before</th>
<th>After</th>
</tr>
</thead>
<tbody>
<tr>
<td><img src="https://github.com/hwding/pdf-unstamper/blob/master/art/before.png"></td>
<td><img src="https://github.com/hwding/pdf-unstamper/blob/master/art/after.png"></td>
</tr>
<tr>
<td><img src="https://github.com/hwding/pdf-unstamper/blob/master/art/before-ituring.png"></td>
<td><img src="https://github.com/hwding/pdf-unstamper/blob/master/art/after-ituring.png"></td>
</tr>
</tbody>
</table>

## Download && Release-Notes
[Releases](https://github.com/hwding/pdf-unstamper/releases).

## Help
```
Usage: 
   [OPTION] -i [INPUT PDF] -k [KEYWORDS...] (-o [OUTPUT PDF])
   [OPTION] -I [INPUT DIR] -k [KEYWORDS...] (-O [OUTPUT DIR])

Options:
   -d,  --directly          directly modify the input file(s), which makes option o/O unnecessary
   -r,  --recursive         process files in the given dir recursively
```

## Example
  ```bash
  # For single file processing
  ➜ java -jar pdf-unstamper.jar -i "C Recipes.pdf" -o "C Recipes.unstamped.pdf" -k www.allitebooks.com
  ➜ java -jar pdf-unstamper.jar -i "RoR.pdf" -o "RoR.unstamped.pdf" -k 图灵社区会员
  # Or
  ➜ java -jar pdf-unstamper.jar -i "C Recipes.pdf" -d -k www.allitebooks.com
  ➜ java -jar pdf-unstamper.jar -i "RoR.pdf" -d -k 图灵社区会员
  
  # For massive files processing
  ➜ java -jar pdf-unstamper.jar -I pdfs/ -O unstampedPdfs/ -r -k www.allitebooks.com
  # Or
  ➜ java -jar pdf-unstamper.jar -I pdfs/ -d -r -k www.allitebooks.com
  ```
## Structure
```
unstamper
├── core
│   └── Processor.java
├── io
│   └── IOHandler.java
├── log
│   └── GeneralLogger.java
├── Main.java
└── util
    ├── OptionManager.java
    ├── TaskRunner.java
    └── TextStampUtil.java
```
