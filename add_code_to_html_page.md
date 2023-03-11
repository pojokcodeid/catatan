```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/highlight.js@11.7.0/styles/atom-one-dark.css">
  <title>Document</title>
</head>
<body>
<h1>Ini Contoh Postingan</h1>
<p>Copy code berikut :</p>
<pre>
  <code>  const add = (x, y) => x + y;
  let result = 0;
  try {
    result = add(10, 20);
  } catch (e) {
    console.log(e.message);
  } finally {
    console.log({ result });
  }
</code></pre>

<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.7.0/highlight.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/highlightjs-line-numbers.js@2.8.0/dist/highlightjs-line-numbers.min.js"></script>
<script>
  hljs.initHighlightingOnLoad();
  hljs.initLineNumbersOnLoad();
</script>
</body>
</html>

<!-- sumber -->
<!-- https://highlightjs.org/download/ -->
<!-- https://www.jsdelivr.com/package/npm/highlight.js?tab=files&path=scss -->
<!-- https://www.jsdelivr.com/package/npm/highlightjs-line-numbers.js?tab=files -->
```
