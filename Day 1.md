# Day 1



Building your first html page.

Preliquisites:

  - A text editor; preferred sublime/Vs code
  - Browser
  

# Creating the file
Go to your text editor and create a new file. On the file menu, choose save as. Make sure the file name is mypage.html. Some text editors might have already chosen the file type for you. If so, change the type to *All files

![save as image](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQn2woBZLmXJYB7UmQOI8utJepWxdDs0SnivnmkOhYehYX_Y7Jg)

# Understanging html syntax
1. All HTML documents must start with a document type declaration: <!DOCTYPE html>.
2. The HTML document itself begins with <html> and ends with </html>.
3. The visible part of the HTML document is between <body> and </body>.
4. Html markup is tag based. an opening tag looks like this 
    <tag>
    A closing tag looks like this
    </tagname>
    
# First test run
copy this code to your text editor where you have mypage.html open
```html
<!DOCTYPE html>
<html>
<body>

<h1>Elon musk</h1>
<p>

Elon Reeve Musk FRS (/ˈiːlɒn/; born June 28, 1971) is a technology entrepreneur, investor, and engineer.[4][5][6] He holds South African, Canadian, and U.S. citizenship and is the founder, CEO, and lead designer of SpaceX;[7] co-founder, CEO, and product architect of Tesla, Inc.;[8] co-founder of Neuralink; founder of The Boring Company;[9] co-founder and initial co-chairman of OpenAI;[10] and co-founder of PayPal. In December 2016, he was ranked 21st on the Forbes list of The World's Most Powerful People.[11] He has a net worth of $19.4 billion and is listed by Forbes as the 40th-richest person in the world.[3]

</p>

</body>
</html>
```

- Save the file
- Open your file browser to where you have save the file
- Right click the file and choose the option open with.
- When displayed with the programs list, choose one browser,for example chrome
- You should see the result as shown below

# Understanding the code

1. The first type tag <!DOCTYPE html> specifies to the browser that the document is a html document.
2. Every other tag, whenever it is opened, there is an accompanying closing tag.
    Example: For the h1(heading 1 tag), there is an opening tag <h1> and after the content that should be part of the heading, there is a closing tag </h1>
3. Html is linearly parsed. Ie if on your code you placed the heading before a paragraph, the expected output is in that same order.


# Practice makes permanent!
- With basic understanding of the above snippet, attempt to alter the headings and paragraphs. Feel free to experiment with other html tags such as
    1. ```<i>italic text</i>```
    2. ```<u>underline text</u>```
    3. ```<strong>Emphasized text</strong>```
    4. ```<a href='google.com'>Link to google </a>```
