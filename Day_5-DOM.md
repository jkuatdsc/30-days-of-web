# Manipulating the DOM (Document Object Model) using JavaScript

JavaScript is capable of manipulating a webpage by creating elements, adding attributes, getting attributes as well as removing elements from a webpage. Other cool things JavaScript is capable of include animating, making network requests such as user authentication and fetching data for from a computer lying somewhere on the internet (server) or API (what allows various services to communicate eg payments and authentication)

For this short tutorial, we are going to query the data submitted from a form and log it on your browser console, add a couple of css attributes as well as add some text into an HTML element, still using JavaScript.

For this exercise, create your `index.html`, add the following boilerplate code into your file.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
    <style>
    body {
        margin: 0;
        padding: 0;
        background-color: #999; /** a shorthand for #999999 */
    }
    </style>
</head>
<body>
    <div id ="root">
        <h1 id="heading"></h1>
    </div> 
      
    <script>
    console.log('Hello there, world')
    </script>
</body>
</html>
```

 Open it on your favorite browser **(as long as it is not Internet Explorer😡)**. Open the browser console (`Ctrl`+ `Shift`+ `I` or `Fn` + `F12`). Move to the `Console` tab highlighted in that section and hopefully you see the `Hello there, World` statement. This is the where JavaScript runs on the browser and you can view your JavaScript errors and statements from here.

For our first example, we will fetch the heading and add some text in it, using Js. You can clear the `console.log('Hello there, world')` and add the following code to the section. 

```javascript
let headingText = document.querySelector('#heading');
headingText.textContent = '🐱‍👤 Developer';
```
In this example, we have used `document.querySelector` and specified the id of `heading`. When using the querySelector, don't forget the `#heading` for ids or `.class` for class attributes. For the  `querySelector()` method, if you have multiple elements sharing a given attribute, it will get only the first one. If you would wish to fetch all elements with specific attributes, `document.querySelectorAll()`

Other DOM manipulator methods we can use are document `document.getElementById()`, `document.getElementsByClassName()`, `document.getElementsByTagName()` and `getElementsByName()`

Let's now add some color and increase the size of our text, therefore, add the following in your styles.

```css
.headingAttr {
    color: crimson;
    font-size: 50px;
}
```
...and let us now create an attribute, and set it to `headingAttr`. Go to the style section of your script and add the following 

```javascript
headingText.setAttribute('class', 'headingAttr')
// or
headingText.classList.add('headingAttr')
```

Both work the same. Feel free to play around with the styles and attributes. There is no right way of doing things, as long as it works, which is the important thing and ensure you have fun.

Let's cover one more concept, event listeners. In a nutshell, event listeners listen for events (probably not the best explanation out there but it is what it is, an event listener) such as `click`, `submit`, `mouseover`, `input`, `change`, `focus` etc. The event listener has two arguments that are compulsory and an optional one (an object containing other options which define behaviour of the given event). For our case, all you need to know for now is that the first argument is the event to be fired, which in our case will be a `click`, and the second argument will be a function containing the application logic to be carried out when it is clicked. For the sake of simplicity, we will only add an alert. If it is too simple for you, feel free to explore the event you wish to fire

Add the following just below the heading.

```html
<button id="btn">Click Me!!</button>
```

... and a little sugar and spicing for our button...

```css
button {
    border: none;
    background-color: darkslategray;
    color: #fff;
    padding: 15px;
    margin: 20px;
    font-size: 20px;
    font-weight: bolder;
}
button:hover{
    opacity: 50%;
}
```
...let's perform some sorcery now...uhhhhm, I meant let's add some code 

```javascript
let btn = document.getElementById('btn');
btn.addEventListener('click', function(){
    alert('You just clicked me and fired an event')
});
```

Save the file and refresh your browser to see the output once you click the button.

Congratulations, you fired your first event, added textContent to the heading element and some styling to your webpage using JavaScript. Hope you are feeling all powerful right now (Enjoy it). For more you can visit w3 schools and Mozilla Developer Network for more details and explore the examples available.

In case you get stuck, refer to the starter file, `index.html` in this repository.

## Happy Hacking 🥳