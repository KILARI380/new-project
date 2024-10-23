# creating personal potfolio using HTML, css and javscript
# index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Developer Portfolio</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
</head>
<body>
    <header>
        <nav>
            <h1><a href="#">My Portfolio</a></h1>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="hero">
        <div class="hero-content">
            <h2>Hello, I'm [Your Name]</h2>
            <p>A passionate web developer</p>
            <a href="#projects" class="btn">View My Work</a>
        </div>
    </section>

    <section id="about" class="section">
        <div class="container">
            <h2>About Me</h2>
            <p>Hi, I'm [Your Name], a front-end developer with a passion for creating responsive and engaging websites. I specialize in JavaScript, React, and creating seamless user experiences.</p>
        </div>
    </section>

    <section id="projects" class="section">
        <div class="container">
            <h2>Projects</h2>
            <div class="project">
                <h3>Project 1: Portfolio Website</h3>
                <p>A modern portfolio website built using HTML, CSS, and JavaScript with smooth scrolling and animations.</p>
                <a href="https://github.com/yourgithub/portfolio" target="_blank"><i class="fab fa-github"></i> View on GitHub</a>
            </div>
            <div class="project">
                <h3>Project 2: To-Do List App</h3>
                <p>A simple and intuitive to-do list application with add, delete, and mark as complete functionality. Built with vanilla JavaScript.</p>
                <a href="https://github.com/yourgithub/todolist" target="_blank"><i class="fab fa-github"></i> View on GitHub</a>
            </div>
        </div>
    </section>

    <section id="skills" class="section">
        <div class="container">
            <h2>Skills</h2>
            <div class="skills-grid">
                <div class="skill">HTML5</div>
                <div class="skill">CSS3</div>
                <div class="skill">JavaScript (ES6+)</div>
                <div class="skill">React.js</div>
                <div class="skill">Node.js</div>
                <div class="skill">Git & GitHub</div>
            </div>
        </div>
    </section>

    <section id="contact" class="section">
        <div class="container">
            <h2>Contact</h2>
            <p>Email: <a href="mailto:youremail@example.com">youremail@example.com</a></p>
            <p>GitHub: <a href="https://github.com/yourgithub" target="_blank">github.com/yourgithub</a></p>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 [Your Name]. All Rights Reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>


# css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Arial', sans-serif;
    background-color: #f4f4f4;
    color: #333;
    scroll-behavior: smooth;
}

header {
    background-color: #333;
    color: white;
    padding: 20px 0;
    position: fixed;
    width: 100%;
    z-index: 1000;
    top: 0;
}

header nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 90%;
    margin: auto;
}

header nav h1 a {
    color: white;
    text-decoration: none;
}

header nav ul {
    display: flex;
    list-style: none;
}

header nav ul li {
    margin-left: 20px;
}

header nav ul li a {
    color: white;
    text-decoration: none;
    font-size: 1.2rem;
    transition: color 0.3s ease;
}

header nav ul li a:hover {
    color: #ff6347;
}

#hero {
    height: 100vh;
    background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://source.unsplash.com/1600x900/?developer') no-repeat center center/cover;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    text-align: center;
}

.hero-content h2 {
    font-size: 3rem;
    animation: fadeIn 1.5s ease;
}

.hero-content p {
    font-size: 1.5rem;
    margin: 20px 0;
    animation: fadeIn 2s ease;
}

.hero-content .btn {
    background-color: #ff6347;
    color: white;
    padding: 10px 20px;
    border-radius: 5px;
    text-decoration: none;
    font-size: 1.2rem;
    animation: fadeIn 2.5s ease;
}

.hero-content .btn:hover {
    background-color: white;
    color: #ff6347;
    transition: background-color 0.3s ease;
}

.section {
    padding: 80px 0;
    background-color: white;
    margin-top: 20px;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: auto;
    text-align: center;
}

h2 {
    font-size: 2.5rem;
    margin-bottom: 20px;
    position: relative;
    display: inline-block;
    animation: slideInLeft 1s ease;
}

h2::after {
    content: '';
    display: block;
    width: 50px;
    height: 4px;
    background-color: #ff6347;
    margin: 10px auto 0;
}

.project, .skill {
    background-color: #f9f9f9;
    padding: 20px;
    border-radius: 10px;
    margin: 20px 0;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    animation: fadeInUp 1s ease;
}

.project a, .project a:hover {
    color: #333;
}

.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
    gap: 10px;
    margin-top: 20px;
}

footer {
    background-color: #333;
    color: white;
    padding: 20px 0;
    text-align: center;
}

@keyframes fadeIn {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
    }
}

@keyframes fadeInUp {
    from {
        transform: translateY(30px);
        opacity: 0;
    }
    to {
        transform: translateY(0);
        opacity: 1;
    }
}

@keyframes slideInLeft {
    from {
        transform: translateX(-100%);
    }
    to {
        transform: translateX(0);
    }
}

# Javscript for interaction
// Smooth Scroll for Anchor Links
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();

        document.querySelector(this.getAttribute('href')).scrollIntoView({
            behavior: 'smooth'
        });
    });
});


# with these html, css and Javascript we can create personal portfolio website.
