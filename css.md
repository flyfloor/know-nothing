### Css

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


#### table cell equal width

```
.table {
  table-layout: fixed;
}
```

#### Css3 transition

transition performance terrible under some Android smart phone, like xiaomi 4.

when use transform, change translateX to translate3d, to use GPU speed up.



### element.getAttribute('style')

element.getAttribute('style') under ie is not working. use element.style.cssText instead.

### Under ie, input type can't change after dom been inserted into document.

### offsetWidth, offsetHeight

normally use offsetWidth and offsetHeight to get element's width, height with padding. but if element 's attribute display is hidden, offsetWidth and offsetHeight will be 0; to calculate element's width and height:

1. set attribute display to block.
2. set visibility to hidden
3. set position to absolute
4. get offsetWidth and offsetHeight
5. recovery changed attributes

### offsetWidth and offsetHeight is 0 can judge whether element is visible.

### Opacity

If set opacity: .5; most browsers will got opacity: 0.5; under ie8, will still be opacity:.5.

