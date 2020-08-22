# CSS and SCSS

This guide is based on airbnb's [javascript CSS/SASS style guide](https://github.com/airbnb/css). Use it as the main reference for css and scss  styling. However, some other rules will be added to fit yello's neccessities.

## Attributes

1. Put declarations in alphabetical order in order to achieve consistent code in a way that is easy to remember and maintain.

```css
background-color: #fff;
height: 24px;
margin: 12px;
width: 8px;
```

2. Don't add vendor prefixes (`-moz`, `-webkit`) as they will be included by the transpiler.
   
3. All the numbers and sizes must be multiples of 4. If there is any inconsistency when using multiple of four numbers, state it in a comment. (I.E. height inputs may vary across different browsers).

## References

* [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html#CSS_Style_Rules)