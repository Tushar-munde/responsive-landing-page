# responsive-landing-page
responsive landing page
 index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav class="navbar">
            <ul class="nav-menu">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home"><h1>Home Section</h1></section>
    <section id="about"><h1>About Section</h1></section>
    <section id="services"><h1>Services Section</h1></section>
    <section id="contact"><h1>Contact Section</h1></section>

    <script src="script.js"></script>
</body>
</html>

styles.css
/* styles.css */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
}

/* Navbar container */
header {
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    background-color: rgba(51, 51, 51, 0.8); /* Semi-transparent background */
    z-index: 1000;
    transition: background-color 0.3s ease; /* Smooth transition */
}

/* Navbar menu */
.navbar {
    display: flex;
    justify-content: center;
    padding: 1em;
}

/* Navbar items */
.nav-menu {
    list-style: none;
    display: flex;
    gap: 2em;
}

.nav-menu li a {
    color: #fff;
    text-decoration: none;
    padding: 0.5em 1em;
    font-size: 1.1em;
    font-weight: 500;
    border-radius: 5px;
    transition: transform 0.2s, background-color 0.3s, color 0.3s;
}

/* Hover effect with scale */
.nav-menu li a:hover {
    background-color: #666;
    color: #ddd;
    transform: scale(1.1); /* Slightly enlarges the item on hover */
}

/* Scrolled effect for navbar */
.navbar.scrolled {
    background-color: rgba(34, 34, 34, 0.9); /* Darker and less transparent when scrolled */
}

/* Section styling */
section {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding-top: 80px; /* Offset for fixed navbar */
    font-size: 2em;
}
 
style.js
// script.js

window.addEventListener('scroll', function() {
    const navbar = document.querySelector('.navbar');
    if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
    } else {
        navbar.classList.remove('scrolled');
    }
});



