# Dude_it-s_CSS

# Box_Model

![box_model](https://github.com/Utsav1256/Dude_it-s_CSS/assets/94625893/caf88dcf-6d88-4585-8749-a0c67bb9a373)

- we have `element` in the middle, we have some `height` and `weight` property applied to it.
- Then, we have `padding` property which is the `internal spacing` of the element.
-Then, after that we have a `border`.
-Then beyond the border we have the `margin`, which is the `external spacing` of ther element.
- All of these properties together are what known as the `Box-Model`.
- We can apply these properties to defferent element in our CSS.
- But we can only apply them to `block level elements`, by that we mean they have a `display type of block` not inline.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./style.css">
    <title>Document</title>
</head>
<body>
    <p>p-tag</p>
    <p>p-tag</p>
    <a href="">a-tag</a>
    <a href="">a-tag</a>
</body>
</html>
```

in Browser:

p-tag     |
          | -> thats because p tags are block elements
p-tag     |

a-tag a-tag | -> thats because a tags are inline elements


- we can only apply those box-model properties to bslock level elements (p tag).
- Block level elements by default take up 100% width of the page.

```css
p, a {
    width: 50%;
    margin: 20px;
    padding: 30px;
    border: 1px solid black;
}
```
- these property will not work as same for the a tags, because ther are inline elements.
- But we can change them from inline to block if we want to
```css
p, a {
    display: block;
}
```
- We can also do something like:
```css
p, a {
    display: inline-block;
    width: 20%;
}
```
- now they will stack out from left to right.
