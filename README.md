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

*font-properties*  
font-weight  
font-family  
typeface, generic typeface  
text-align  

*border*  
size, type of border, color  
`border: 10px solid black;`  
`  border-top: 0px;`  
the specific border modifications should be specified after normal border.  

*padding*  
pushes border by specified size, it is inside the border  

*margin*  
spacing outside the border, helpful to maintain spacing between multiple objects  

all these border, padding and margin has 4 values, top, bottom, left, and right.  

`<div></div>` <- invisible block which are used to separate content.  

## JavaScript
inspect elements -> sources -> snippets -> "type code here"  

*Data type:*  
String, number, boolean  

*code:*  
`alert("Hello" + myName);`  <- pop up message  
`prompt("What is your name?");` <- a pop in which user can input  
`var myName="Angela";` <- stores the string in the new variable  
`myName="jane";` <- replaces the value in the variable  
`console.log();` <- prints in terminal / console  

`Math.random();`  
`Math.round();`

`array.push()` <- insert values in array  
`array.pop()` <- output values in array  

## DOM
*inline javascript*  
`<body onload="alert('Hello')">...</body>` <- to utilize javascript with html  

*internal javascrip*  
```html
<script type="text/javascript">
  alert("Hello");
</script>
```

*external javascript*  
`<script src="index.js" charset="utf-8"></script>` <- mostly used and very easy to implement. Best practice to put this just before body closing tag.  

`document.firstElementChild.lastElementChild;` <- these help target objects in an html file, and can be manipulated to change their properties from the console itself.  
`target.innerHTML = "changed value";` <- to do DOM manipulation
`document.getElementsByTagName("li")` <- returns an array with all the `li` elements  
`document.getElementById("main");` <- returns the element with `main` as id  
`document.querySelector(#id)` <- `#id` for selecting id, `.class` for selecting class, `li a` to select list element with anchor tag, `li.item` then only the 1st item is returned back when there are multiple candidates  
`document.querySelectorAll(#list .item);` <- then it returns an array for all the candidates who match this query  
`document.querySelector().classList.add("anotherClass");` <- `classList` to show classes of selected element, `add()` to add another class to the selected element, `.remove()` to remove class, and `.toggle()` to toggle it on and off. Useful to apply css properties using js.  
`document.querySelector().attribute` <- to see all the targetted element's attribute, `getAttribute()` to see the value of that attribute, `setAttribute()` to apply the value to targetted attribute  

## Node.js
`node` <- in terminal to start the REPL  
`.help` <- for commands  
`.clear` or `ctrl+c` <- to abort current expression  
`.exit` or `ctrl+d` <- to exit REPL  
`.load` <-  to load js from a file into the REPL session  
`.save` <- Save all evaluated commands in this REPL session to a file  

[documentation]('https://nodejs.org/docs/latest-v18.x/api/fs.html#fsreadfilepath-options-callback') <- Useful for future command uses  

To create/write into a file:  
```js
fs.writeFile("message.txt", "Hello", (err) => {
  if (err) throw err;
  console.log("Ran successfully");
});
```

To read a file in string/utf8:  
```js
fs.readFile("message.txt","utf8", (err,data) => {
  if (err) throw err;
  console.log(data);
});
```

For NPM:  
```js
import { randomSuperhero } from "superheroes";
const name = randomSuperhero();
```
