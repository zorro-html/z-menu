# `<z-menu>`

Menu element whose item can be chosen by click

- only show `<li>` and `<hr>` child elements
- supported `:hover`, `:active`, `:focus`, `[disabled]` status
- `<li>` items could bt clicked and fire an event with `event.detail.selected`
- `<li>` items with `[disabled]` could not be clicked.

## Events

- `select`

## Examples

```
<style>
  .container::before,
  .container::after {content: ""; clear: both; display: table;}
</style>

<p>You are choosing: <label id="z-menu-selected"></label></p>

<div class="container">
  <z-menu id="z-menu-test" style="float: left;">
    <li>ITEM</li>
    <li>ITEM 2</li>
    <li disabled>ITEM 3</li>
    <hr>
    <li>ITEM 4</li>
  </z-menu>
</div>

<script>
  var label = document.querySelector('html /deep/ #z-menu-selected');
  var menu = document.querySelector('html /deep/ #z-menu-test');

  menu.addEventListener('select', function (event) {
    label.textContent = event.detail.selected.textContent;
  });
</script>
```
