<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pricing Table App</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f9;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      margin: 0;
    }
    .pricing-container {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
      justify-content: center;
    }
    .card {
      background: #fff;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      width: 280px;
      text-align: center;
      padding: 20px;
      transition: transform 0.3s ease;
    }
    .card:hover {
      transform: translateY(-10px);
    }
    .card h3 {
      margin-bottom: 10px;
      font-size: 1.5rem;
    }
    .price {
      font-size: 2rem;
      margin: 15px 0;
      color: #2196F3;
    }
    ul {
      list-style: none;
      padding: 0;
      margin: 20px 0;
    }
    ul li {
      margin: 10px 0;
    }
    button {
      background: #2196F3;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 5px;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #1976D2;
    }
    .highlight {
      border: 2px solid #2196F3;
    }
  </style>
</head>
<body>
  <div class="pricing-container">
    <div class="card">
      <h3>Basic</h3>
      <p class="price">$9/mo</p>
      <ul>
        <li>✔ 5 Projects</li>
        <li>✔ Basic Support</li>
        <li>✔ Community Access</li>
      </ul>
      <button>Select</button>
    </div>

    <div class="card highlight">
      <h3>Standard</h3>
      <p class="price">$19/mo</p>
      <ul>
        <li>✔ 20 Projects</li>
        <li>✔ Priority Support</li>
        <li>✔ Advanced Features</li>
      </ul>
      <button>Select</button>
    </div>

    <div class="card">
      <h3>Premium</h3>
      <p class="price">$29/mo</p>
      <ul>
        <li>✔ Unlimited Projects</li>
        <li>✔ 24/7 Support</li>
        <li>✔ All Features</li>
      </ul>
      <button>Select</button>
    </div>
  </div>

  <script>
    const buttons = document.querySelectorAll("button");
    buttons.forEach(btn => {
      btn.addEventListener("click", () => {
        alert(`You selected the ${btn.parentElement.querySelector("h3").textContent} plan!`);
      });
    });
  </script>
</body>
</html>
