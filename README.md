# WebDevelopment
## HTML
***Notes:***  
mozilla.org to check for more tags  
*content element*  
`<h1></h1>` <- heading 1 to 6   
`<p></p>` <- paragraph element  

*void element*  
`<hr />` <- horizontal rule (basically divides content with a line)  
`<br />` <- break (adds space between lines)  

*list element*  
`<ul>`  
`  <li></li>` <- list elements  
`  <li></li>`  
`  <li></li>`  
`</ul>` <- unordered list  
`<ol></ol>` <- ordered list  
These lists can also be nested and indentation is a must to help with these issues.  

*anchor elements*  
`<a href="link", draggable= true></a>` <- link / url  
there are more global attributes, that helps us customize stuff.  

*images*  
it is also a void element because it doesn't have a closing tag  
`<img src="url/number" alt="Alternate text to describe the image">` <- image and url is location of the image and `/number` gives the size.  

## CSS
Cascading Style Sheet.  

3 ways to apply css:  
- Internal: `<style>css</style>`
- Inline: `<tag style="css" />`
- External: `<link href="style.css"/>`

Inline: Useful for applying styles to one page, tedious if you have multiple sites, not recommended.  
```html
<html style="background:blue">
  ...
</html>
```

Internal: Applying to one document, not recommended for multiple sites.  
```html
<html>
  <head>
    <style>
      html {
        background  =red;
      }
    </style>
  </head>
</html>
```  

External: Useful for multiple sites, and has its own separate file.  
```html
<html>
  <head>
    <link 
      rel = "stylesheet"
      href = "./styles.css"
      />
  </head>
</html>
```
css file:  
```css
html {
  background : green;
}
```

Here, `h1` is the css selector. and every `h1` element will follow the same style.  
```css
h1 {
  color: blue;
}
```

Class selector, here we can add this class to group similar elements so all elements follow the same rule. We use the `.` followed by the class name to apply it.  
```css
.red-text {
  color: red;
}
```

```html
<h2 class="red-text">Red</h2>
<h2>Blue</h2>
<h2>Green</h2>
<p class="red-text">Paragraph</p>
```  

ID selector, applied to only one element which has that id. Only 1 id per document.  
```css
#main {
  color: red;
}
```  

```html
<h2 id="main"> Main </h2>
<h2> random </h2>
```

Attribute selector, it selects all the html element `p` with the attribute `draggable` and apply the style to them.  
```css
p[draggable="true"]{
  color: red;
}
```

```html
<p draggable="true"> Drag this </p>
<p draggable="false"> Do not drag this </p>
```

universal selector, selects all.  
```css
* {
  color: red;
}
```

*properties*  
background-color  
color  
`colorhunt.co` for colour palletes  

