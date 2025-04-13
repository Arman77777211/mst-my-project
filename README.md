<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Document</title>
    
</head>
<body>
    
    <header class="site-header">
        <div class="container">
          <h1>My Awesome Site</h1>
          <nav>
            <ul class="nav-list">
              <li><a href="#">Home</a></li>
              <li><a href="#">Services</a></li>
              <li><a href="#">Contact</a></li>
            </ul>
          </nav>
        </div>
      </header>
    
      <main>
        <section style="height: 200px; padding: 20px;">
          <p>Scroll down to test the sticky header...</p>
        </section>
      </main>

<!-- Video Section -->
<section class="video-section">
    <div class="container">
      <h2>Watch Our Video</h2>
      <div class="video-container">
        <iframe width="100%" height="500" src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
    </div>
  </section>
  <!-- HTML Form Example -->
<form id="contact-form">
    <input type="text" name="name" placeholder="Enter your name" required>
    <input type="email" name="email" placeholder="Enter your email" required>
    <textarea name="message" placeholder="Your message" required></textarea>
    <button type="submit">Send</button>
  </form>
  
  
  


    <script src="main.js"></script>
</body>
</html>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  body {
 font-family: sans-serif;
    line-height: 1.6;
  }
  
  
  .site-header {
    position: sticky;
    top: 0;
    z-index: 999;
    background-color: rgba(0, 0, 0, 0.8);
    color: #fff;
    padding: 15px 20px;
    backdrop-filter: blur(5px);
  }
  
  .container {
    max-width: 1200px;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .nav-list {
    list-style: none;
    display: flex;
    gap: 20px;
  }
  
  .nav-list a {
    color: white;
    text-decoration: none;
    transition: color 0.5s;
  }
  
  .nav-list a:hover {
    color: #ffd700; /* gold hover */
  }
  
  
/* Video Section */
.video-section {
    padding: 50px 20px;
    background-color: #f4f4f4;
  }
  
  .video-section h2 {
    text-align: center;
    font-size: 28px;
    color: #333;
    margin-bottom: 20px;
  }
  
  .video-container {
    max-width: 800px;
    margin: auto;
  }
  
  @media (max-width: 768px) {
    .video-container iframe {
      height: 300px;
    }
  }
  
  
const button = document.querySelector('button');

button.addEventListener('mouseover', function() {
  button.style.transform = 'scale(1.1)';  
  button.style.transition = 'transform 0.3s';
});

button.addEventListener('mouseout', function() {
  button.style.transform = ''; 
});
window.addEventListener('scroll', function() {
    const header = document.querySelector('.site-header');
    if (window.scrollY > 50) {
        header.classList.add('scrolled');
    } else {
        header.classList.remove('scrolled');
    }
});
const form = document.querySelector("#contact-form");
form.addEventListener("submit", function(event) {
    event.preventDefault();
    alert("Your message has been sent!");
});
  



