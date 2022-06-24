---
layout: default
---
<html>
<head>
<title>GESTOFS-develop</title>
<style type="text/css" media="all">
            /* h1, h2, h3 and p are in Times New Roman font */
            h1, h2, h3, p, li {
                font-family: "Times New Roman";
            }

figcaption {
  color: black;
  font-family: "Times New Roman";
  text-align: center;
}
ul.a {
  list-style-type: circle;
}

ul.b {
  list-style-type: square;
}
ol {
    counter-reset: list;
}
ol > li {
    list-style: none;
}
ol > li:before {
    content: counter(list) ") ";
    counter-increment: list;
}
</style>

</html>
