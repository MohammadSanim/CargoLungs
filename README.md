<!DOCTYPE html>
<html>
<head>
    <title>Zinsco Group</title>
    <style>
        /* body {
    margin: 0;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: cornsilk;
}

ul {
    padding: 0;
    list-style-type: none;
}

ul li {
    box-sizing: border-box;
    width: 15em;
    height: 3em;
    font-size: 20px;
    border-radius: 0.5em;
    margin: 0.5em;
    box-shadow: 0 0 1em rgba(0,0,0,0.2);
    color: white;
    font-family: sans-serif;
    text-transform: capitalize;
    line-height: 3em;
    transition: 0.3s;
    cursor: pointer;
}

ul li:nth-child(odd) {
    background: linear-gradient(to right, orange, tomato);
    text-align: left;
    padding-left: 10%;
    transform: perspective(500px) rotateY(45deg);
}

ul li:nth-child(even) {
    background: linear-gradient(to left, orange, tomato);
    text-align: right;
    padding-right: 10%;
    transform: perspective(500px) rotateY(-45deg);
}

ul li:nth-child(odd):hover {
    transform: perspective(200px) rotateY(45deg);
    padding-left: 5%;
}

ul li:nth-child(even):hover {
    transform: perspective(200px) rotateY(-45deg);
    padding-right: 5%;
}
 */
    </style>
    <script>
        // const article = document.querySelector('article');

// to compute the center of the card retrieve its coordinates and dimensions
const {
  x, y, width, height,
} = article.getBoundingClientRect();
const cx = x + width / 2;
const cy = y + height / 2;

// following the mousemove event compute the distance betwen the cursor and the center of the card
function handleMove(e) {
  const { pageX, pageY } = e;

  // ! consider the relative distance in the [-1, 1] range
  const dx = (cx - pageX) / (width / 2);
  const dy = (cy - pageY) / (height / 2);

  // rotate the card around the x axis, according to the vertical distance, and around the y acis, according to the horizontal gap 
  this.style.transform = `rotateX(${10 * dy * -1}deg) rotateY(${10 * dx}deg)`;
}

// following the mouseout event reset the transform property
function handleOut() {
  this.style.transform = 'initial';
}

article.addEventListener('mousemove', handleMove);
article.addEventListener('mouseout', handleOut);

    </script>
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home">HOME</a></li>
                <li><a href="#about">ABOUT US</a></li>
                <li><a href="#freight">FREIGHT FORWARD</a></li>
                <li><a href="#services">SERVICES</a></li>
                <li><a href="#companies">OUR COMPANIES</a></li>
                <li><a href="#contact">CONTACT US</a></li>
                <li><a href="#join">JOIN US</a></li>
                <li><a href="#location">LOCATION</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section id="home">
            <!-- Home content goes here -->
        </section>
        <section id="about">
            <!-- About Us content goes here -->
        </section>
        <section id="freight">
            <!-- Freight Forward content goes here -->
        </section>
        <section id="services">
            <!-- Services content goes here -->
        </section>
        <section id="companies">
            <!-- Our Companies content goes here -->
        </section>
        <section id="contact">
            <!-- Contact Us content goes here -->
        </section>
        <section id="join">
            <!-- Join Us content goes here -->
        </section>
        <section id="location">
            <!-- Location content goes here -->
        </section>
    </main>
    <footer>
        <!-- Footer content goes here -->
    </footer>
</body>
</html>
