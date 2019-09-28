# Day 2

Adding a navigation bar, table and  to your website

Prerequisites:
* Text editor of choice
* Browser

## Let's get started😃

* Create a new file in your working folder and call it `index.html` .
* Create another file and call it `styles.css` --- this is where all your fancy styles will live.
* Open the folder in your favorite text editor and start building...
* Paste the following code in `index.html`, 

```
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <!-- Our navigation bar -->
  <nav>
     <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">News</a></li>
      <li><a href="#">Contact</a></li>
      <li><a href="#">About</a></li>
    </ul> 
  </nav>
  <!-- Our heading -->
  <h1>List of actors and their approximated net worth</h1>
  <p>**These values are randomly guessed values</p>
  <!-- Our table -->
  <table>
      <tr>
        <th>Firstname</th>
        <th>Lastname</th>
      <th>Worth</th>
      </tr>
      <tr>
        <td>Dwayne</td>
        <td> Johnson</td>
        <td>$100m</td>
      </tr>
      <tr>
        <td>Robert</td>
        <td>Dmwney Jnr</td>
        <td>$75m</td>
      </tr>
      <tr>
        <td>Angelina</td>
        <td> Jolie</td>
        <td>$80m</td>
      </tr>
      <tr>
        <td>Cleveland</td>
        <td>Brown</td>
        <td>$90m</td>
      </tr>
    </table>
</body>
</html>
```
 * Save the file
 * Open the file in the browser
 * This is the following expected output
 
![save as image](https://raw.githubusercontent.com/jkuatdsc/30-days-of-web/master/images/html.png)

In the code above, the `<link/>` tag makes reference to all your styles that you will add to your webpage.

## Let's spice things up

Go back to your editor and open up `styles.css`

Paste the following in the file

```
/* Let's add some default styles for the entire 
webpage such as setting spacing and margin to 0.
 */
body {
	font-family: Arial, sans-serif;
	padding: 0;
	margin: 0;
}
/* by default, an unordered list will have a rounded bullet in front of it
  let's therefore remove the bullet points by setting the list style type to none
*/
ul {
	list-style-type: none;
}
/* this aligns the list items to the left side of the web page */
li {
	float: left;
}

/* Let's style the links on our webpage */
li a {
	display: block;
	color: white;
	text-align: center;
	padding: 14px 16px;
	text-decoration: none;
}

/* Change the link color to #111 (black) on hover */
li a:hover {
	background-color: #111;
}

/* add some style to the table */
table {
	border-collapse: collapse;
	width: 100%;
}

th,
td {
	padding: 8px;
	text-align: left;
	border-bottom: 1px solid lightblue;
}

/*  Give the title of the page some life *?
h1 {
	color: teal;
}
```
Save the file and refresh your browser. 
Your output should look like something like this.

![save as file](https://raw.githubusercontent.com/jkuatdsc/30-days-of-web/master/images/output.png)

** Don't worry if you don't understand everything in the files, there are snippets to guide you through it. Tinker with the markup and styles in the files to have a better understanding of how things work under the hood. 
For more html and css practice and tips, read through [W3 Schools](https://www.w3schools.com/) and explore what is possible with html and css. 
In case of any challenges faced in understanding, feel free to ask for help
