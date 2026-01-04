# Harsh-Industries
Basic website pages for my industry. 

HTML format 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>HARSH INDUSTRIES</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f5f5f5;
      color: #333;
    }

    header {
      background-color: #0f172a;
      color: white;
      padding: 20px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }

    .logo {
      font-size: 28px;
      font-weight: bold;
      letter-spacing: 1px;
    }

    nav {
      display: flex;
      align-items: center;
      gap: 20px;
      position: relative;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: 600;
      transition: color 0.3s ease;
    }

    nav a:hover {
      color: #38bdf8;
    }

    .dropdown {
      position: relative;
    }

    .dropdown-content {
      display: none;
      position: absolute;
      top: 35px;
      background-color: #ffffff;
      min-width: 180px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
      z-index: 1;
      border-radius: 5px;
    }

    .dropdown-content a {
      color: #0f172a;
      padding: 10px 15px;
      text-decoration: none;
      display: block;
      font-weight: 500;
    }

    .dropdown-content a:hover {
      background-color: #f0f0f0;
    }

    .dropdown:hover .dropdown-content {
      display: block;
    }

    .search-box {
      display: flex;
      gap: 10px;
      align-items: center;
    }

    .search-box input[type="text"] {
      padding: 7px 10px;
      border-radius: 5px;
      border: none;
      outline: none;
    }

    .search-box button {
      background-color: #38bdf8;
      color: white;
      padding: 8px 12px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      font-weight: bold;
      transition: background-color 0.3s ease;
    }

    .search-box button:hover {
      background-color: #0ea5e9;
    }

    .hero {
      background: url('https://images.unsplash.com/photo-1581579185169-dc3e0b1e5aa2') center/cover no-repeat;
      color: white;
      text-align: center;
      padding: 100px 20px;
      background-blend-mode: multiply;
      background-color: rgba(0, 0, 0, 0.5);
    }

    .hero h1 {
      font-size: 48px;
      margin-bottom: 10px;
    }

    .hero p {
      font-size: 20px;
      margin-bottom: 0;
    }

    main {
      padding: 40px 20px;
      max-width: 1200px;
      margin: auto;
    }

    h2 {
      text-align: center;
      margin-bottom: 30px;
      font-size: 32px;
      color: #0f172a;
    }

    .about,
    .products {
      margin-bottom: 50px;
    }

    .about p {
      font-size: 18px;
      line-height: 1.6;
      max-width: 900px;
      margin: auto;
      text-align: center;
    }

    .products-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
      margin-top: 30px;
    }

    .product {
      background-color: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
      text-align: center;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .product:hover {
      transform: translateY(-5px);
      box-shadow: 0 6px 16px rgba(0, 0, 0, 0.15);
    }

    .product h3 {
      color: #1e293b;
      margin-bottom: 10px;
    }

    .product p {
      font-size: 16px;
      font-weight: bold;
      color: #0284c7;
    }

    .hidden {
      display: none;
    }

    footer {
      background-color: #0f172a;
      color: white;
      text-align: center;
      padding: 20px;
      font-size: 14px;
    }
  </style>
</head>
<body>

<header>
  <div class="logo">HARSH INDUSTRIES</div>
  <nav>
    <a href="#">Home</a>

    <div class="dropdown">
      <a href="#">Locations ▾</a>
      <div class="dropdown-content">
        <a href="#">Rajkot (Main Branch)</a>
        <a href="#">Delhi</a>
        <a href="#">Mumbai</a>
        <a href="#">Ahmedabad</a>
      </div>
    </div>

    <div class="dropdown">
      <a href="#">Contact ▾</a>
      <div class="dropdown-content">
        <a href="tel:8200964465">Harsh Makadia - 8200964465</a>
        <a href="tel:8460184469">Jayesh Makadia - 8460184469</a>
        <a href="tel:9725820678">Piyush Sinojiya - 9725820678</a>
      </div>
    </div>

    <div class="search-box">
      <input type="text" id="searchInput" placeholder="Search products...">
      <button onclick="searchProducts()">Search</button>
    </div>
  </nav>
</header>

<section class="hero">
  <h1>Welcome to HARSH INDUSTRIES</h1>
  <p>Leaders in Stainless Steel Scrubbers & Foam Pads</p>
</section>

<main>
  <section class="about">
    <h2>About Us</h2>
    <p>HARSH INDUSTRIES is a trusted name in stainless steel scrubbers and foam pads. Our products are designed for durability, quality, and effective cleaning. We proudly serve homes and industries across the country.</p>
    <p><strong>Owners:</strong> Harsh Makadia, Jayesh Makadia, Piyush Sinojiya</p>
  </section>

  <section class="products">
    <h2>Our Products</h2>
    <div class="products-grid" id="productList">
      <div class="product"><h3>Small Size Steel Scrubber</h3><p>₹10</p></div>
      <div class="product"><h3>Medium Size Steel Scrubber</h3><p>₹15</p></div>
      <div class="product"><h3>Large Size Steel Scrubber</h3><p>₹20</p></div>
      <div class="product"><h3>Extra Large Size Steel Scrubber</h3><p>₹25</p></div>
      <div class="product"><h3>Foam Scrub Pad (Without Wire)</h3><p>₹8</p></div>
      <div class="product"><h3>Foam Scrub Pad (With Wire)</h3><p>₹12</p></div>
    </div>
  </section>
</main>

<footer>
  &copy; 2025 HARSH INDUSTRIES. All rights reserved.
</footer>

<script>
  function searchProducts() {
    const input = document.getElementById('searchInput').value.toLowerCase();
    const products = document.querySelectorAll('#productList .product');

    products.forEach(product => {
      const title = product.querySelector('h3').textContent.toLowerCase();
      if (title.includes(input)) {
        product.style.display = 'block';
      } else {
        product.style.display = 'none';
      }
    });
  }
</script>

</body>
</html>
