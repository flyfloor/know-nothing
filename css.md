### Css weird

#### table-cell

when use `table` or `display as table`, set the height of `table-cell` element will not be right. 
table cell' height will according to the content in it. so need to add a content:

```
.table
  .table-cell
    .content // assign line-height, height
```

table display is very usefull,for 'some reason' can't use flex display, it's easy to display as table,for example:

```
input + submit need to be fluid at bottom of form.
```

can write as:

```
.table
  input.table-cell style="width:100%"
  .table-cell style="width:5em"
    submit stype="display:block"
```
