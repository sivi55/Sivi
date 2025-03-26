# Sivi
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pinterest-inspired Clothing Aesthetics</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Header -->
  <header>
    <div class="logo">
      <h1>Fashion Aesthetic</h1>
    </div>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Explore</a></li>
        <li><a href="#">My Favorites</a></li>
      </ul>
    </nav>
  </header>

  <!-- Main Content -->
  <main>
    <section class="grid-container">
      <div class="grid-item">
        <img src="https://via.placeholder.com/400x600?text=Boho+Style" alt="Boho Style">
        <p>Boho Style</p>
      </div>
      <div class="grid-item">
        <img src="https://via.placeholder.com/400x600?text=Streetwear+Style" alt="Streetwear Style">
        <p>Streetwear Style</p>
      </div>
      <div class="grid-item">
        <img src="https://via.placeholder.com/400x600?text=Vintage+Style" alt="Vintage Style">
        <p>Vintage Style</p>
      </div>
      <div class="grid-item">
        <img src="https://via.placeholder.com/400x600?text=Minimalist+Style" alt="Minimalist Style">
        <p>Minimalist Style</p>
      </div>
      <div class="grid-item">
        <img src="https://via.placeholder.com/400x600?text=High+Fashion+Style" alt="High Fashion Style">
        <p>High Fashion Style</p>
      </div>
    </section>
  </main>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 Fashion Aesthetic | All Rights Reserved</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

/* General Styling */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background-color: #f5f5f5;
  color: #333;
}

header {
  background-color: #333;
  color: white;
  padding: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

header .logo h1 {
  font-size: 24px;
  letter-spacing: 2px;
}

nav ul {
  list-style-type: none;
}

nav ul li {
  display: inline;
  margin: 0 15px;
}

nav ul li a {
  text-decoration: none;
  color: white;
  font-weight: bold;
}

main {
  padding: 20px;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
}

.grid-item {
  background-color: white;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  text-align: center;
}

.grid-item img {
  width: 100%;
  height: auto;
  transition: transform 0.3s ease;
}

.grid-item img:hover {
  transform: scale(1.05);
}

.grid-item p {
  padding: 15px;
  font-size: 18px;
  background-color: #fff;
  color: #555;
  font-weight: bold;
}

footer {
  text-align: center;
  padding: 20px;
  background-color: #333;
  color: white;
}

document.addEventListener('DOMContentLoaded', () => {
  const gridItems = document.querySelectorAll('.grid-item');
  
  gridItems.forEach(item => {
    item.addEventListener('mouseover', () => {
      item.style.transform = "scale(1.05)";
    });

    item.addEventListener('mouseout', () => {
      item.style.transform = "scale(1)";
    });
  });
});
