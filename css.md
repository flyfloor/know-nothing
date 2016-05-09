### Css weird

#### table-cell

when use `table` or `display as table`, set the height of `table-cell` element will not be right. 
table cell' height will according to the content in it. so need to add a content:

```
.table
  .table-cell
    .content // assign line-height, height
```
