# code-blocks


# Web Dev

## IOS

### IOS disable zoom

[Source: Stackoverflow](https://stackoverflow.com/a/50823326)

For some reason, IOS disabled the meta viewport tag `user-scalable=no` which is supposed to disable zoom on a page. Sometimes you are creating an app and it needs to disable zoom. Paste this at the bottom of your HTML file:

```
<script type="text/javascript">
  document.addEventListener('touchmove', function (event) {
    if (event.scale !==1 ){ event.preventDefault(); }
  }, { passive: false });
</script>
```
