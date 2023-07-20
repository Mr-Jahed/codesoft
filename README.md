# codesoft
This is a web development Course which is fullfilled using HTML CSS and JS
This Is a Landing Page(site)
(HTML CODE)
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="index2.css">
    <title>Document</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
</head>

<body>
    <header>
        <header>
            <section class="nav">
                <div class="logo">
                    <a href="#"><i class="fas fa-utensils"></i>food</a>
                </div>
                <input id="menu-toggle" type="checkbox" />
                <label class='menu-button-container' for="menu-toggle">
                    <div class='menu-button'></div>
                </label>
                <ul class="menu">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#speciality">About</a></li>
                    <li> <a href="#popular">Popular</a></li>
                    <li> <a href="#review">Contact</a></li>
                    <li> <a href="#order" class="order">Menu</a></li>
                </ul>
            </section>
            <section class="home" id="home ">
                <div class="content">
                    <h3 class="mainfont">
                        The Ch<span class="yellowColor">ee</span>se Decker
                    </h3>
                    <h3>
                        fastest f<span class="yellowColor">oo</span>d for , instant
                        <span class="yellowColor">Hunger</span>
                    </h3>
                    <p>
                    </p>
                    <a href="# " class="btn">ORDER NOW</a>
                </div>
                <div class="image">
                    <img src="pizza.jpg" alt=" " />
                </div>
            </section>
        </header>
    </header>
</body>

</html>


(CSS CODE)
@import url("https://fonts.googleapis.com/css2?family=Jacques+Francois+Shadow&display=swap");

* {
    font-family: "Nunito", sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    outline: none;
    border: none;
    text-decoration: none;
    text-transform: capitalize;
    transition: all 0.2s linear;
}

html {
    font-size: 62.5%;
    overflow: hidden;
}

body {
    background: #212531;
    margin: 0;
}

header {
    margin: 0px;
}

a {
    text-decoration: none;
    color: #000;
}

ul {
    list-style: none;
}

/* styling the logo  */

.logo {
    font-size: 2.5rem;
    font-weight: bolder;
    color: #666;
    display: inline-block;
}

.logo i {
    padding-right: 2rem;
    color: black;
}

.order {
    text-shadow: -1px -1px 0 yellow, 1px -1px 0 yellow, -1px 1px 0 yellow, 1px 1px yellow;
}

/* Stying the navbar container */

.nav {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    background: white;
    color: black;
    height: 65px;
    padding: 1em;
    font-size: 25px;
}

.menu li:hover {
    cursor: pointer;
    transform: scale(1.2);
}

.menu {
    display: flex;
    flex-direction: row;
    list-style-type: none;
    margin: 0;
}

.menu>li {
    margin: 0 1rem;
    overflow: hidden;
}

/*Container for menu button  */

.menu-button-container {
    display: none;
    height: 100%;
    width: 30px;
    cursor: pointer;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

#menu-toggle {
    display: none;
}

/*  Creating the hamburger menu button  */

.menu-button,
.menu-button::before,
.menu-button::after {
    display: block;
    background-color: black;
    position: absolute;
    height: 6px;
    width: 32px;
    border-radius: 3px;
    color: white;
}

.menu-button::before {
    content: "";
    margin-top: -8px;
}

.menu-button::after {
    content: "";
    margin-top: 8px;
}

/*  Adding Functionality to the Hamburger Menu with CSS  */

#menu-toggle:checked+.menu-button-container .menu-button::before {
    margin-top: 0px;
    transform: rotate(45deg);
}

#menu-toggle:checked+.menu-button-container .menu-button {
    background: rgba(255, 255, 255, 0);
}

#menu-toggle:checked+.menu-button-container .menu-button::after {
    margin-top: 0px;
    /*  transforms the hamburger icon into a cross  */
    transform: rotate(-45deg);
}

/* media queries  */

@media (max-width: 991px) {
    html {
        font-size: 55%;
    }

    header {
        padding: 2rem;
    }

    section {
        padding: 2rem;
    }
}

@media (max-width: 768px) {
    .menu-button-container {
        display: flex;
    }

    .menu {
        position: absolute;
        top: 0;
        margin-top: 50px;
        left: 0;
        flex-direction: column;
        width: 100%;
        justify-content: center;
        align-items: center;
        padding: 2rem
    }

    .menu li:hover {
        transform: scale(1);
    }

    #menu-toggle~.menu li {
        height: 0;
        margin: 0;
        padding: 0;
        border: 0;
    }

    #menu-toggle:checked~.menu li {
        border: 1px solid #9f9a9a;
        height: 2.5em;
        padding: 0.5em;
    }

    .menu>li {
        display: flex;
        justify-content: center;
        margin: 0;
        padding: 0.5em 0;
        width: 100%;
        color: black;
        background-color: #e8e8e8;
    }

    .menu>li:not(:last-child) {
        border-bottom: 1px solid #444;
    }
}

/* Styling the hero section */

.home {
    display: flex;
    flex-wrap: wrap;
    gap: 1.5rem;
    min-height: 100vh;
    align-items: center;
}

.home .content {
    flex: 1 1 40rem;
    padding-top: 6.5rem;
}

/* Styling the main image */

.home .image {
    flex: 1 1 30rem;
}

.home .image img {
    width: 90%;
    height: 90%;
    padding: 1rem;
    animation: float 3s linear infinite;
}

/* animating the main image   */

@keyframes float {

    0%,
    100% {
        transform: translateY(0rem);
    }

    50% {
        transform: translateY(3rem);
    }
}

.home .content h3 {
    font-size: 5rem;
    color: white;
}

/* Styling the content */

.yellowColor {
    color: yellow;
}

.mainfont {
    font-family: "Jacques Francois Shadow", cursive;
}

.home .content p {
    font-size: 1.7rem;
    color: white;
    padding: 1rem 0;
}

.heading {
    text-align: center;
    font-size: 3.5rem;
    padding: 1rem;
    color: #666;
}

/* Styling the button  */

.btn {
    display: inline-block;
    padding: 0.8rem 3rem;
    border: 0.2rem solid white;
    color: white;
    cursor: pointer;
    font-size: 1.7rem;
    border-radius: 0.5rem;
    position: relative;
    overflow: hidden;
    z-index: 0;
    margin: 1rem 1rem 0 0;
}

.btn:hover {
    color: #fff;
}

/* Adding media queries to make it responsive   */
@media (max-width: 450px) {
    html {
        font-size: 50%;
        overflow-x: hidden;
        overflow-y: scroll;
        text-align: center;
    }
}
