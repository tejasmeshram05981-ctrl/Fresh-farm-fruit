# Fresh-farm-fruit
Fresh farm fruit and organic fruit 
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fresh Farm Fruit</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #eef7ee;
    }
    header {
      background: #2e7d32;
      color: white;
      padding: 15px;
      text-align: center;
      font-size: 22px;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
      gap: 15px;
      padding: 15px;
    }
    .card {
      background: white;
      padding: 10px;
      border-radius: 15px;
      text-align: center;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    .card img {
      width: 100%;
      height: 120px;
      border-radius: 10px;
    }
    .btn {
      margin-top: 8px;
      padding: 8px;
      width: 100%;
      background: #4caf50;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
    .cart {
      position: fixed;
      bottom: 0;
      width: 100%;
      background: white;
      padding: 10px;
      box-shadow: 0 -2px 10px rgba(0,0,0,0.2);
    }
    .cart button {
      width: 100%;
      padding: 12px;
      background: #25D366;
      color: white;
      border: none;
      border-radius: 10px;
      font-size: 16px;
    }
  </style>
</head>
<body><header>Fresh Farm Fruit 🍎</header><div class="products">  <div class="card">
    <img src="https://via.placeholder.com/150" />
    <h3>Apple</h3>
    <p>₹120/kg</p>
    <button class="btn" onclick="addToCart('Apple - 120₹')">Add</button>
  </div>  <div class="card">
    <img src="https://via.placeholder.com/150" />
    <h3>Mango</h3>
    <p>₹150/kg</p>
    <button class="btn" onclick="addToCart('Mango - 150₹')">Add</button>
  </div>  <div class="card">
    <img src="https://via.placeholder.com/150" />
    <h3>Banana</h3>
    <p>₹50/dozen</p>
    <button class="btn" onclick="addToCart('Banana - 50₹')">Add</button>
  </div></div><div class="cart">
  <button onclick="orderWhatsApp()">Order on WhatsApp</button>
</div><script>
let cart = [];

function addToCart(item) {
  cart.push(item);
  alert(item + " added!");
}

function orderWhatsApp() {
  if(cart.length === 0){
    alert("Cart empty!");
    return;
  }

  let message = "Hello, I want to order:\n" + cart.join("\n");
  let phone = "919876543210"; // apna number yaha change karo
  let url = "https://wa.me/" + phone + "?text=" + encodeURIComponent(message);

  window.open(url, '_blank');
}
</script></body>
</html>
