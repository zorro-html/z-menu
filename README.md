# menu

菜单

* 只会显示子 `<li>` 和子 `<hr>` 元素
* 有 `:hover`, `:active`, `:focus`, `[disabled]` 的状态
* 没有 `[disabled]` 状态的 `<li>` 可以被点击，会触发 `select` 事件，被点击的元素会被写入 `event.detail.selected`

# Example

```
<jie-menu>
  <li>ITEM</li>
  <li>ITEM 2</li>
  <li disabled>ITEM 3</li>
  <hr>
  <li>ITEM 4</li>
</jie-menu>

<script>
  var menu = document.querySelector('jie-menu');

  menu.addEventListener('select', function (e) {
    // e.detail.selected
  });
</script>
```
