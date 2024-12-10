# c11finalproject
index.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Travel Landing Page</title>
  </head>
  <body>
    <section class="showcase">
      <header>
        <h2 class="logo">Travel</h2>
        <div class="toggle"></div>
      </header>
      <video
        src="https://designsupply-web.com/samplecontent/vender/codepen/20181014.mp4"
        muted
        loop
        autoplay
      ></video>
      <!-- Download Video Source and host the file on your own server -->
      <!-- For example: https://www.pexels.com/video/aerial-view-of-beautiful-resort-2169880/ -->
      <div class="overlay"></div>
      <div class="text">
        <h2>Never Stop</h2>
        <h3>Exploring The World</h3>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias animi
          provident unde illum fuga culpa enim eos amet ullam explicabo.
        </p>
        <a href="#">Explore</a>
      </div>
      <ul class="social">
        <li>
          <a href="#"><img src="https://i.ibb.co/x7P24fL/facebook.png" /></a>
        </li>
        <li>
          <a href="#"><img src="https://i.ibb.co/Wnxq2Nq/twitter.png" /></a>
        </li>
        <li>
          <a href="#"><img src="https://i.ibb.co/ySwtH4B/instagram.png" /></a>
        </li>
      </ul>
    </section>
    <div class="menu">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">News</a></li>
        <li><a href="#">Destination</a></li>
        <li><a href="#">Blog</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </div>
    <script src="script.js"></script>
  </body>
</html>



script.js


const menuToggle = document.querySelector(".toggle");
const showcase = document.querySelector(".showcase");

menuToggle.addEventListener("click", () => {
  menuToggle.classList.toggle("active");
  showcase.classList.toggle("active");
});

style.css

@import url("https://fonts.googleapis.com/css?family=Poppins:200,300,400,500,600,700,800,900&display=swap");

:root {
  --overlay-color: #31385c;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

.showcase {
  position: absolute;
  right: 0;
  width: 100%;
  min-height: 100vh;
  padding: 100px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #111;
  color: #fff;
  transition: 0.5s;
  z-index: 2;
}

.showcase.active {
  right: 300px;
}

.showcase header {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  padding: 40px 100px;
  z-index: 1000;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  text-transform: uppercase;
  cursor: pointer;
}

.toggle {
  position: relative;
  width: 60px;
  height: 60px;
  background: url(https://i.ibb.co/HrfVRcx/menu.png);
  background-repeat: no-repeat;
  background-size: 30px;
  background-position: center;
  cursor: pointer;
}

.toggle.active {
  background: url(https://i.ibb.co/rt3HybH/close.png);
  background-repeat: no-repeat;
  background-size: 25px;
  background-position: center;
  cursor: pointer;
}

.showcase video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  min-height: 100vh;
  object-fit: cover;
  opacity: 0.8;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: var(--overlay-color);
  mix-blend-mode: overlay;
}

.text {
  position: relative;
  z-index: 10;
}

.text h2 {
  font-size: 5em;
  font-weight: 800;
  line-height: 1em;
  text-transform: uppercase;
}

.text h3 {
  font-size: 4em;
  font-weight: 700;
  line-height: 1em;
  text-transform: uppercase;
}

.text p {
  font-size: 1.1em;
  font-weight: 400;
  margin: 20px 0;
  max-width: 700px;
}

.text a {
  display: inline-block;
  font-size: 1em;
  background: #fff;
  padding: 10px 30px;
  text-decoration: none;
  color: #111;
  margin-top: 10px;
  text-transform: uppercase;
  letter-spacing: 2px;
  transition: 0.2s;
}

.text a:hover {
  letter-spacing: 6px;
}

.social {
  position: absolute;
  bottom: 20px;
  z-index: 10;
  display: flex;
  justify-content: center;
  align-items: center;
}

.social li {
  list-style: none;
}

.social li a {
  display: inline-block;
  filter: invert(1);
  margin-right: 20px;
  transform: scale(0.5);
  transition: 0.5s;
}

.social li a:hover {
  transform: scale(0.5) translateY(-15px);
}

.menu {
  position: absolute;
  top: 0;
  right: 0;
  width: 300px;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.menu ul {
  position: relative;
  list-style: none;
}

.menu ul li a {
  text-decoration: none;
  font-size: 24px;
  color: #111;
}

.menu ul li a:hover {
  color: var(--overlay-color);
}

@media (max-width: 800px) {
  .showcase,
  .showcase header {
    padding: 40px;
  }

  .text h2 {
    font-size: 3em;
  }

  .text h3 {
    font-size: 2em;
  }
}
