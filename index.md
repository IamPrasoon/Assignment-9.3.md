
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Responsive Landing Page</title>
<style>
* { box-sizing: border-box; }
body { margin: 0; font-family: Arial; }

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
    padding: 20px;
    background: navy;
    color: white;
}
nav { display: flex; gap: 20px; flex-wrap: wrap; }
nav a { color: white; text-decoration: none; }

.hero {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    gap: 30px;
    padding: 40px;
    background: lightblue;
}
.hero img { width: 100%; max-width: 400px; height: auto; }

.features {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 20px;
    padding: 30px;
}
.card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    background: #eee;
    padding: 20px;
    border-radius: 10px;
}
button {
    padding: 12px;
    background: orange;
    border: none;
    cursor: pointer;
}
footer {
    background: navy;
    color: white;
    text-align: center;
    padding: 20px;
}

@media (max-width: 600px) {
    .hero, .features { grid-template-columns: 1fr; }
    .hero { padding: 20px; }
    header { flex-direction: column; }
}
</style>
</head>
<body>
<header>
    <h2>CodeWithPrasoon</h2>
    <nav>
        <a href="#home">Home</a>
        <a href="#features">Features</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<main>
    <section class="hero" id="home">
        <div>
            <h1>Learn Web Development</h1>
            <p>Build modern websites using HTML, CSS and JavaScript.</p>
            <button onclick="location.href='#features'">Get Started</button>
        </div>
        <img src="coding.jpg" alt="Coding illustration">
    </section>

    <section class="features" id="features">
        <div class="card">
            <h3>HTML</h3>
            <p>Learn website structure.</p>
        </div>
        <div class="card">
            <h3>CSS</h3>
            <p>Design beautiful webpages.</p>
        </div>
        <div class="card">
            <h3>JavaScript</h3>
            <p>Add website interactivity.</p>
        </div>
    </section>
</main>

<footer id="contact">
    <p>&copy; 2026 Prasoon Anand</p>
</footer>
</body>
</html>
