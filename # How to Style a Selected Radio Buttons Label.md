# How to Style a Selected Radio Buttons Label

```html
<div class="radio-toolbar">
  <input type="radio" id="radio1" name="radios" value="all" checked>
  <label for="radio1">All</label>

  <input type="radio" id="radio2" name="radios" value="false">
  <label for="radio2">Open</label>

  <input type="radio" id="radio3" name="radios" value="true">
  <label for="radio3">Archived</label>
</div>
```
主要是用到一个CSS选择器`+` 
B + E ：元素B的任一下一个兄弟元素E
```CSS
    .radio-toolbar input[type="radio"] {
      display: none;
    }

    .radio-toolbar label {
      display: inline-block;
      background-color: #ddd;
      padding: 4px 11px;
      font-family: Arial;
      font-size: 16px;
      cursor: pointer;
    }

    .radio-toolbar input[type="radio"]:checked+label {
      background-color: #bbb;
    }
```

[在线演示](http://jsbin.com/katemofega)
