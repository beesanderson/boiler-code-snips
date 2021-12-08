# Responsive Mega Simple Navbar Hamburger Menu

```CSS
/* 
==================================================================================================================================================================
Hey all! Bridgette Sanderson here 🥸🤓😬

Feel free to use this as you would like, take or add to as you see fit :D 

This is just a mega simple default navbar code snip I made for myself for "ease of access." 


PS- If you link to give me credit or shout outs that would be infinitely appreciated
but is totally not necessary! I'm still very new to the <devCommunity> 
and am in need of a job yesterday...or a month ago if you catch my drift. 
So any kudos is always appreciated AND most importantly ALWAYS reciprocated!!! 

Happy Coding and love to all my fellow DEVS!!! :D
💗Bridgette Sanderson 
12/8/2021
                                                                    🥸 🤓 😬
==================================================================================================================================================================
*/
```

located in `/navbar-basic` folder (duh lol)

Code Snips: 
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Navbar Refactor</title>
    <link href="/navbar-basics/navbar.css" rel="stylesheet">
</head>
<body>

<nav class="navbar">
    <div class="navbar-header">
        <p class="navbar-title">Bridgette Sanderson<span class="navbar-subtitle block">Software && Web Developer</span></p>
    </div>

    <!-- put ham menu between two current divs -->
    <a href="#" class="toggle-button" id="toggle-button">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
    </a>

    <div class="navbar-links">
        <ul>
            <li><a href="#" class="active-page">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Projects</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </div>
</nav>
        

    <script src="/navbar-basics/navbar.js"></script>
</body>
</html>


```

```CSS
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    padding: 0;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #333;
    color: #fff;
}

.navbar-title {
    font-size: 2rem;
    margin: .5rem;
}

.navbar-subtitle {
    display: block;
    font-size: 1rem;
    margin-top: -.6rem;
    margin-left: 4.5rem;
}

.navbar-links ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
}


.navbar-links li a {
    text-decoration: none;
    padding: 1rem;
    display: block;
    color: #fff;
}


.navbar-links li:hover {
    background: #5555;
}


.toggle-button {
    position: absolute;
    top: .75rem;
    right: 1rem;
    display: none;
    flex-direction: column;
    justify-content: space-between;
    width: 40px;
    height: 30px;
}


.toggle-button .bar {
    height: 3px;
    width: 100%;
    background: #fff;
    border-radius: 10px;
}

@media (max-width: 600px) {

    .toggle-button {
        display: flex;
    }

    .navbar-links {
        display: none;
        width: 100%;
    }

    .navbar {
        flex-direction: column;
        align-items: flex-start;
    }

    .navbar-links ul {
        width: 100%;
        flex-direction: column;
    }

    .navbar-links li {
        text-align: center;
    }

    .navbar-links li a {
        padding: .5rem 1rem;
    }

    .navbar-links.active {
        display: flex;
    }
}
```

```JAVASCRIPT
const toggleButton = document.getElementsByClassName('toggle-button')[0]
const navbarLinks = document.getElementsByClassName('navbar-links')[0]

console.log(navbarLinks)

toggleButton.addEventListener("click", () => {
    navbarLinks.classList.toggle("active")
})
```
Can add animation through downloading an `npm` package from `animate.css` or linking through bootstrap's CDN if you don't want to download. Will help with site's runtime/load time in some cases. 

- Of course you can always write your own animation which is something I personally enjoy doing as its something I've done since I was a kid :) 
