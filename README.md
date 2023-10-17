# Dude_it-s_CSS

# CSS Positioning

## Box_Model

![box_model](https://github.com/Utsav1256/Dude_it-s_CSS/assets/94625893/caf88dcf-6d88-4585-8749-a0c67bb9a373)

- we have `element` in the middle, and we have some `height` and `weight` properties applied to it.
- Then, we have `padding` property which is the `internal spacing` of the element.
  -Then, after that, we have a `border`.
  -Then beyond the border, we have the `margin`, which is the `external spacing` of the element.
- All of these properties together are what is known as the `Box-Model`.
- We can apply these properties to different elements in our CSS.
- But we can only apply them to `block level elements`, by that we mean they have a `display type of block` not inline.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="./style.css" />
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
![Screenshot (140)](https://github.com/Utsav1256/Dude_it-s_CSS/assets/94625893/3f32e114-7360-4040-b99e-e027f91b4821)

- that's because `p tags` are block elements 
- and `a tags` are inline elements

- we can only apply those box-model properties to block-level elements (p tag).
- Block-level elements by default take up 100% width of the page.

```css
p,
a {
  width: 50%;
  margin: 20px;
  padding: 30px;
  border: 1px solid black;
}
```

- these properties will not work the same for the `a tags`, because they are inline elements.
- Inline elements stack from left to right
- But we can change them from inline to block if we want to

```css
p,
a {
  display: block;
}
```

- We can also do something like:

```css
p,
a {
  display: inline-block;
  width: 20%;
}
```

- now they will stack out from left to right.

## Normal Document Flow

```html
<body>
  <p>Hii Buddy!</p>
  <p>How are you?</p>
  <p>How are you doing?</p>
</body>
```

in Browser:
![Screenshot (139)](https://github.com/Utsav1256/Dude_it-s_CSS/assets/94625893/870f5fb3-281b-4473-964e-13ffd3157f5f)

- The normal document flow is from top to bottom.

## Floating Elements

- Floating is one of the most used techniques in page layouts for positioning content.
- And it lets us position an element to the very left or the very right of a parent element and in doing so it removes itself from that Normal Document Flow that we have been talking about.
- Initially, it was designed so that a developer could wrap text around an image, but nowadays it's useful for other things too, like making text columns or grid galleries, etc.

### Let's wrap a text around the image

```html
<body>
  <img src="./images/personal.png" alt="" width="150px" height="160px" />
  <p>Personal growth</p>
</body>
```

in Browser :
![Screenshot (138)](https://github.com/Utsav1256/Dude_it-s_CSS/assets/94625893/6b32f6f2-5658-48c0-b4a6-5766bae1c16e)

- Here, we can see whats happening, is the paragraph is going below the image, that is Normal Document Flow, right!!

- Now we will add float property here:

```css
img {
  float: left;
}
```

in Browser:
![Screenshot (137)](https://github.com/Utsav1256/Dude_it-s_CSS/assets/94625893/07d54c78-1206-4c65-b346-64d67d8237d3)

- it is floating the image to the left-most area of the parent element.

- we are taking it out from the Normal Document Flow and we are positioning it to the very left of the document or the very left of the parent element.

```css
img {
  float: right;
}
```
![Screenshot (136)](https://github.com/Utsav1256/Dude_it-s_CSS/assets/94625893/0d5b7142-5e96-49c9-a24c-970a7a09feb5)

- it is floating the image to the right-most area of the parent element.
