# Graphviz in the browser

Served at <https://rsms.me/graphviz/>

Use in your own things:

```html
<head>
  <meta charset="utf-8">
  <script src="https://rsms.me/graphviz/graphviz.js"></script>
</head>
<body>
<script>
graphviz.layout(`
digraph {
  Hello -> World
  Hej -> Hello
  Värld -> World -> Hej
}
`).then(svg => {
  document.body.innerHTML = svg
})
</script>
</body>
```

This is essentially a wrapper around [viz.js](https://github.com/mdaines/viz.js).
