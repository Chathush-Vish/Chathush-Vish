### Hi there 👋
<!DOCTYPE html>
<html lang="en">
   <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <title>PetiCare - eCommerce</title>

      <!-- Stylesheet -->
      <link rel="stylesheet" href="./style.css" />

      <!-- Boootstrap icons cdn -->
      <link
         rel="stylesheet"
         href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.1/font/bootstrap-icons.css"
         integrity="sha384-4LISF5TTJX/fLmGSxO53rV4miRxdg84mZsxmO8Rx5jGtp/LbrixFETvWa5a6sESd"
         crossorigin="anonymous"
      />
      <style>
         @import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

         * {
            padding: 0;
            margin: 0;
            box-sizing: border-box;
            transition: all ease-in-out 0.2s;
         }

         body {
            font-family: "Poppins", sans-serif;
         }

         ul {
            list-style: none;
         }

         a {
            color: #222;
            text-decoration: none;
         }

         button {
            cursor: pointer;
         }

         .top-nav {
            width: 100%;
            height: 80px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 10px 150px;
            z-index: 99;
         }

         .product-container {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 50px;
            width: 100%;
            height: 80vh;
         }

         .product {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
         }
         .product div {
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 100%;
            margin-top: 20px;
            padding: 0 20px;
         }

         .product .amount {
            width: 50%;
         }

         #add-cart {
            width: 100%;
            padding: 10px;
            margin-top: 20px;
            border: none;
            background-color: #3779fc;
            color: aliceblue;
         }
         #add-cart:hover {
            background-color: #e3e4e7;
            color: #222;
            transition: 0.2s;
            cursor: pointer;
         }

         .cart-container {
            display: none;
            width: 100%;
            height: 100vh;
            position: fixed;
            z-index: 9999;
            top: 0;
            left: 0;
         }
         .dark-area {
            width: 75%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.6);
            display: flex;
            align-items: center;
            justify-content: center;
         }
         .cart-area {
            background-color: #fff;
            padding: 50px 0px;
            width: 25%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: start;
            flex-direction: column;
            gap: 30px;
         }

         .cart-product-area {
            width: 100%;
            height: 75%;
            padding: 0 20px;
            display: flex;
            flex-direction: column;
            gap: 10px;
            overflow-y: scroll;
         }
         .empty-show {
            width: 100%;
            height: 75%;
            display: flex;
            align-items: center;
            justify-content: center;
         }

         .cart-product {
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 30px;
            padding: 10px 20px;
            border-bottom: 1px solid #e3e4e7;
         }
         .cart-product .details {
            width: 100%;
            display: flex;
            flex-direction: column;
            gap: 10px;
         }

         .cart-product div div {
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 100%;
         }

         .cart-product .amount i {
            color: #686868;
            cursor: pointer;
         }

         .cart-product .amount i:hover {
            color: #222;
         }

         .remove-cart {
            background-color: #f0f0f0;
            padding: 5px 0;
            border: none;
            color: #222;
         }

         .remove-cart:hover {
            background-color: #3a3a3a;
            color: #fff;
         }

         .cart-area .check {
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            width: 100%;
            gap: 15px;
            padding: 0 20px;
            border-top: 1px solid #e3e4e7;
            padding-top: 20px;
         }

         .cart-area .check .check-btns {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 10px;
         }

         .check-btns {
            width: 100%;
         }

         .check-btns button {
            width: 100%;
            height: 40px;
            font-size: 14px;
            border: none;
         }

         #clear-cart {
            background-color: #e3e4e7;
            color: #222;
         }

         #check-btn {
            background-color: #3779fc;
            color: #fff;
         }

         #check-btn:hover,
         #clear-cart:hover {
            background-color: #222;
            color: #fff;
         }

         .cart-link {
            position: relative;
         }

         .cart-dot {
            display: none;
            position: absolute;
            top: 26px;
            right: 135px;
            background-color: #3779fc;
            width: 8px;
            height: 8px;
            border-radius: 50%;
         }

         .bi-bag {
            font-weight: bold;
            font-size: 25px;
         }
      </style>
   </head>
   <body>
      <!-- Header -->
      <header class="header">
         <nav class="top-nav">
            <a href="#">
               <img src="./src/logo.png" width="150" alt="" />
            </a>
            <ul class="nav-links">
               <li class="nav-link .cart-link">
                  <a href="#" id="cart-open"><i class="bi bi-bag"></i></a>
                  <div class="cart-dot"></div>
               </li>
            </ul>
         </nav>
      </header>
      <!-- End of Header -->

      <!-- Product area -->
      <section class="product-container">
         <!-- products -->
      </section>
      <!-- End of Product area -->

      <!-- Cart-area -->
      <section class="cart-container">
         <div class="dark-area" id="cart-close"></div>

         <div class="cart-area">
            <!-- cart title -->
            <p>Your Cart</p>
            <!-- cart-prodcts display -->
            <div class="cart-product-area">
               <!-- Cart products -->
            </div>
            <!-- total and ceackouts-->
            <div class="check">
               <div class="total-price">
                  <!-- total price -->
               </div>
               <div class="check-btns">
                  <button id="clear-cart" onclick="clearCart()">
                     Clear Cart
                  </button>
                  <button id="check-btn">Go to Checkout</button>
               </div>
            </div>
         </div>
      </section>
      <!-- End of Cart-area -->

      <!-- JavaScript -->
      <script src="./main.js"></script>
   </body>
</html>

<!--
**Chathush-Vish/Chathush-Vish** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
