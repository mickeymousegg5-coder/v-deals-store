

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vishal Deal Store</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial;background:#f4f5f9;color:#222}
header{background:#182848;color:white;padding:20px;text-align:center}
header h1{margin:0;color:#ffd54f}
.search{padding:15px;text-align:center;background:white}
.search input{width:90%;max-width:500px;padding:13px;border:1px solid #ccc;border-radius:25px}
nav{display:flex;justify-content:center;gap:20px;padding:15px;background:#243b55;flex-wrap:wrap}
nav a{color:white;text-decoration:none;font-weight:bold}
.hero{padding:35px 15px;text-align:center;background:linear-gradient(120deg,#182848,#4b6cb7);color:white}
.hero h2{font-size:28px}
.container{padding:20px;max-width:1100px;margin:auto}
.products{display:grid;grid-template-columns:repeat(auto-fit,minmax(145px,1fr));gap:15px}
.card{background:white;padding:12px;border-radius:12px;text-align:center;box-shadow:0 2px 8px #ddd}
.card img{width:100%;height:140px;object-fit:contain}
.card h3{font-size:16px}
.price{color:#087b38;font-weight:bold}
button{background:#ff9800;color:#fff;border:0;padding:11px 18px;border-radius:7px;font-weight:bold;cursor:pointer}
footer{text-align:center;background:#182848;color:white;padding:25px;margin-top:30px}
</style>
</head>
<body>

<header>
<h1>🛍️ VISHAL DEAL STORE</h1>
<p>Smart Shopping | Best Deals</p>
</header>

<div class="search">
<input type="text" id="search" placeholder="Search products..." oninput="filterProducts()">
</div>

<nav>
<a href="#home">Home</a>
<a href="#products">Products</a>
<a href="#deals">Best Deals</a>
<a href="#contact">Contact</a>
</nav>

<section class="hero" id="home">
<h2>Welcome to Vishal Deal Store</h2>
<p>Discover amazing products and exciting deals</p>
<button onclick="document.getElementById('products').scrollIntoView()">Shop Now</button>
</section>

<div class="container" id="products">
<h2>🔥 Popular Products</h2>
<div class="products" id="productList">

<div class="card">
<img src="https://placehold.co/300x200?text=Headphones">
<h3>Wireless Headphones</h3>
<p class="price">Check Latest Price</p>
<button onclick="buy('HEADPHONES')">Buy Now</button>
</div>

<div class="card">
<img src="https://placehold.co/300x200?text=Watch">
<h3>Smart Watch</h3>
<p class="price">Check Latest Price</p>
<button onclick="buy('WATCH')">Buy Now</button>
</div>

<div class="card">
<img src="https://placehold.co/300x200?text=Speaker">
<h3>Bluetooth Speaker</h3>
<p class="price">Check Latest Price</p>
<button onclick="buy('SPEAKER')">Buy Now</button>
</div>

<div class="card">
<img src="https://placehold.co/300x200?text=Shoes">
<h3>Sports Shoes</h3>
<p class="price">Check Latest Price</p>
<button onclick="buy('SHOES')">Buy Now</button>
</div>

</div>
</div>

<footer id="contact">
<h3>Vishal Deal Store</h3>
<p>Thank you for visiting our store!</p>
<p>Contact: Add your business email here</p>
<p>Affiliate Disclosure: We may earn a commission from qualifying purchases.</p>
</footer>

<script>
function buy(product){
alert("Product link will be added soon: "+product);
}
function filterProducts(){
let value=document.getElementById("search").value.toLowerCase();
document.querySelectorAll(".card").forEach(card=>{
card.style.display=card.innerText.toLowerCase().includes(value)?"block":"none";
});
}
</script>

</body>
</html>
