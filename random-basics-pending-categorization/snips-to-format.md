## To make ul or ol list two columns

```HTML
Create HTML¶
Use the <ul> element for an unordered list and add <li> elements.
<ul>
  <li>Some text</li>
  <li>Some text</li>
  <li>Some text</li>
  <li>Some text</li>
  <li>Some text</li>
  <li>Some text</li>
</ul>
```
```CSS
Add CSS¶
Use the columns property and specify “2” as a value. Also, add the -webkit- and -moz- prefixes.
ul {
  columns: 2;
  -webkit-columns: 2;
  -moz-columns: 2;
}
```