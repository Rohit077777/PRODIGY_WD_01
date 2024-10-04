<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Navigation Menu</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
    }

    .navbar {
      position: fixed;
      top: 0;
      width: 100%;
      background-color: #333;
      padding: 10px;
      z-index: 1000;
      transition: background-color 0.3s ease;
    }

    .nav-list {
      display: flex;
      justify-content: center;
      list-style-type: none;
    }

    .nav-item {
      margin: 0 15px;
    }

    .nav-item a {
      text-decoration: none;
      color: white;
      padding: 10px;
      font-size: 18px;
      transition: color 0.3s ease;
    }

    .nav-item a:hover {
      color: #ff9800;
    }

    .content {
      padding-top: 80px; /* To avoid content being hidden under the fixed navbar */
    }

    section {
      padding: 50px;
      height: 100vh;
    }

    #home {
      background-color: #f4f4f4;
    }

    #about {
      background-color: #e2e2e2;
    }

    #services {
      background-color: #cfcfcf;
    }

    #contact {
      background-color: #b0b0b0;
    }

    .scrolled {
      background-color: #111 !important; /* Change navbar background color when scrolled */
    }
  </style>
</head>
<body>

  <nav class="navbar" id="navbar">
    <ul class="nav-list">
      <li class="nav-item"><a href="#home">Home</a></li>
      <li class="nav-item"><a href="#about">About</a></li>
      <li class="nav-item"><a href="#services">Services</a></li>
      <li class="nav-item"><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <div class="content">
    <section id="home">
      <h1>Home</h1>
      <p>Welcome to the homepage.</p>
    </section>

    <section id="about">
      <h1>About Us</h1>
      <p>Learn more about us here.</p>
    </section>

    <section id="services">
      <h1>Services</h1>
      <p>We offer a wide range of services.</p>
    </section>

    <section id="contact">
      <h1>Contact Us</h1>
      <p>Get in touch with us.</p>
    </section>
  </div>

  <script>
    // Change navbar style on scroll
    window.addEventListener("scroll", function() {
      const navbar = document.getElementById("navbar");
      if (window.scrollY > 50) {
        navbar.classList.add("scrolled");
      } else {
        navbar.classList.remove("scrolled");
      }
    });
  </script>

</body>
</html>

