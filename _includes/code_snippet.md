{% assign code = include.code %}
{% assign language = include.language %}

``` {{ language }}
{{ code }}
```

<textarea id="code" style="display:none;">{{ code | xml_escape }}</textarea>
<button id="copybutton" data-clipboard-target="#code">
  Copy
</button>

<script>
var copybutton = document.getElementById('copybutton');
var clipboard = new Clipboard(copybutton);

clipboard.on('success', function(e) {
    console.log(e);
});
clipboard.on('error', function(e) {
    console.log(e);
});
</script>
