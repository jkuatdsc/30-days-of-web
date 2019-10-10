# Building layouts using flex box

The Flexible Box Layout Module, makes it easier to design flexible responsive layout structure without using float or positioning.

For this example, we will be building the layout below.


The first subdivisions are easy. A header, a main section and a footer.

```html
    <header class="bg-primary">
    </header>

    <main>
    </main>

    <footer class="bg-primary">
    </footer>
```

Within the main section, the team section has three subdivisions. We can apply flex box to divide the team section to three equal parts.

```html
        <div class="flex-container">

            <div class="team-item">
                <div class="team-item-body">
                        
                </div>
            </div>

            <div class="team-item">
                    <div class="team-item-body">
                            
                    </div>
                </div>
            
            <div class="team-item">
                    <div class="team-item-body">
                            
                    </div>
                </div>

        </div>

```

The parent flex container sets the display to flex and specifies the orientation to a row.
Every team item section sets a flex-bias of 25% and flex grow of 0. It will give to all elements in row 25% width. They will not grow and go one by one.


The flex css is outlined below

```css
    .flex-container {
            display: flex;
            flex-direction: row;
            justify-content: center;

        }

        .team-item{
            flex-basis: 25%;
            flex-grow: 0;
            padding: 8px;
            min-height:100px;
            
        }

        .team-item-body{
            box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
            transition: 0.3s;
        }
```

The final result is something like this.
![screenshot](./images/flex-intro.png)

More properties of flex box can be found here.
[W3School CSS3 flex box](https://www.w3schools.com/css/css3_flexbox.asp) .The source code to this introduction to flex box can be found [here](./code/flex.html)

### Happy coding!!!
