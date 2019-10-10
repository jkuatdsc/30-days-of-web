**CSS Grid**

CSS Grid Layout (aka "Grid"), is a two-dimensional grid-based layout system that aims to do nothing less than completely change the way we design grid-based user interfaces. CSS has always been used to lay out our web pages, but it's never done a very good job of it.

First, we used tables, then floats, positioning and inline-block, but all of these methods were essentially hacks and left out a lot of important functionality (vertical centering, for instance). Flexbox helped out, but it's intended for simpler one-dimensional layouts, not complex two-dimensional ones (Flexbox and Grid actually work very well together).

Grid is the very first CSS module created specifically to solve the layout problems we've all been hacking our way around for as long as we've been making websites.

For today's example, create your `index.html` and `style.css` files and copy and paste the following:

```html
    <section class="heading">
      <a href="#"> DSC Web</a>
		</section>

    <section>
      <div class="about">
        <h2>What we're all about</h2>
        <p>
          The Google Developer Group (GDG) Jomo Kenyatta University of
          Agriculture and Technology(JKUAT) chapter is for everyone interested
          in learning about Google technologies and has a passion for building
          what's next using these technologies. Everyone from students to
          professionals and technology enthusiasts is invited to join in.
        </p>
        <p>
          Developer Student Club(DSC) Jomo Kenyatta University of Agriculture
          and Technology(JKUAT) chapter is a Google Developers program for
          university students, designed to help them build their mobile and web
          development skills and knowledge. It is open to any student, ranging
          from novice developers who are just starting, to advanced developers
          who want to further their skills. It is intended to be a space for
          students to learn and collaborate as they solve mobile and web
          development problems.
        </p>
        <p>
          We host our meetups at JKUAT main campus, Juja and are open to the
          general public and everyone is invited to participate. We periodically
          host joint weekly meetups with the Society of Computer Science and
          Information Technology (SCOSIT) at JKUAT.
        </p>
        <p>
          <em>Disclaimer:</em>
          GDG|DSC JKUAT is an independent group; our activities and the opinions
          expressed on here should in no way be linked to Google, the
          corporation.
        </p>
      </div>
      <div class="team">
        <h2>Meet the team</h2>
        <div class="cards">
          <div class="card">
            <img
              src="http://www3.pictures.zimbio.com/gi/Premiere+Summit+Entertainment+Mechanic+Resurrection+b6GqLIsbrDIx.jpg"
              alt="image"
            />
            <p>
							<h1>Jason Statham</h1>
							<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius voluptatem iste expedita minus nisi necessitatibus deserunt </p>
						</p>
          </div>
          <div class="card">
            <img
              src="https://upload.wikimedia.org/wikipedia/commons/5/55/Grace_Hopper.jpg"
              alt="image"
						/>
						<p>
							<h1>Grace Hopper</h1>
							<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius voluptatem iste expedita minus nisi necessitatibus deserunt </p>

						</p>
          </div>
          <div class="card">
            <img
              src="https://www.theedgesusu.co.uk/wp-content/uploads/2016/07/Benedict-Cumberbatch-1-2.jpg"
              alt="image"
						/>
						<p>
							<h1>Benedict Cumberbatch</h1>
							<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius voluptatem iste expedita minus nisi necessitatibus deserunt </p>

						</p>
          </div>
        </div>
      </div>
    </section>

    <section class="footer">
      <p>&copy; 2019 | All Rights Reserved</p>
    </section>
```

```css
@import url("https://fonts.googleapis.com/css?family=Montserrat:400,700&display=swap");

body {
  font-family: "Montserrat", sans-serif;
  padding: 0;
  margin: 0;
  line-height: 1.5rem;
}
h1,
h2 {
  font-weight: 700;
}
h1 {
  font-size: 2rem;
}
h2 {
  font-size: 1.7rem;
}
a {
  text-decoration: none;
  color: #444;
}
/* header */

.heading {
  background: #70a1ff;
  width: 100vw;
  padding: 30px;
}
.heading a {
  text-transform: uppercase;
  font-weight: 700;
  font-size: 30px;
  padding: 20px;
}
/* about */

.about {
  max-width: 800px;
  margin: 20px auto;
}
.about h2 {
  text-align: center;
}
.team h2 {
  text-align: center;
}
.card {
  border: 1px solid #fff;
  box-shadow: 2px 6px 25px rgba(0, 0, 0, 0.1);
}
.card img {
  width: 100%;
  background-size: cover;
  height: 300px;
}

/* footer */
.footer {
  position: relative;
  bottom: 0;
}

.footer p {
  text-align: center;
}
```

As you can see, the three cards on the page are a little messy and all over the page. In this case, we will use CSS Grid to make them responsive to the page by setting minimum width, maximum with:

```css
.cards {
  display: grid;
  grid-gap: 30px;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  margin: 20px;
}
```

We first set `display: grid` on the page, the same way we can set display to inline or block. Grid gap represents the space that will be between the various grid items on the page. `grid-template-colums` represents how many elements will be displayed in a single column. `repeat()` notation allows us to set repeating items on a page, if we had many elements to be displayed on the page, and in our case, it's set to auto-fit. A number may be used such as 2, 8, 4 etc. 

`minmax()` defines the minimum and maximum width an element should occupy in the given space. 

`1fr` is a unit that was introduced with CSS grid and it means 1 fractional unit. It calculates automatically the space needed to be occupied.

For more learning resources: 
* [Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
* [An interactive game for learning Grid](https://cssgridgarden.com/)
* [CSS Grid.io - a free course by Wes Box](https://cssgrid.io/)
