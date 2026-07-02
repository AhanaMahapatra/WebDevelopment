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
```
<html style="background:blue">
  ...
</html>
```

Internal: Applying to one document, not recommended for multiple sites.  
```
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
```
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
```
html {
  background : green;
}
```
