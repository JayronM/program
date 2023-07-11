# program
 <!DOCTYPE html>
<html>
<head>
  <title>Restaurant</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }

    h1 {
      text-align: center;
    }

    .tabs {
      display: flex;
      justify-content: center;
      margin-bottom: 20px;
    }

    .tab {
      padding: 10px 20px;
      background-color: #ccc;
      cursor: pointer;
      margin-right: 10px;
    }

    .tab.active {
      background-color: #f0f0f0;
    }

    .content {
      display: none;
    }

    .content.active {
      display: block;
    }
  </style>
  <script>
    function openTab(tabName) {
      var i, tabContent, tabLinks;
      tabContent = document.getElementsByClassName("content");
      for (i = 0; i < tabContent.length; i++) {
        tabContent[i].style.display = "none";
      }
      tabLinks = document.getElementsByClassName("tab");
      for (i = 0; i < tabLinks.length; i++) {
        tabLinks[i].className = tabLinks[i].className.replace(" active", "");
      }
      document.getElementById(tabName).style.display = "block";
      event.currentTarget.className += " active";
    }
  </script>
</head>
<body>
  <h1>Restaurant</h1>

  <div class="tabs">
    <div class="tab active" onclick="openTab('menu')">Menu</div>
    <div class="tab" onclick="openTab('about')">About</div>
  </div>

  <div id="menu" class="content active">
    <h2>Menu</h2>
    <p>Here you can find our delicious menu items:</p>
    <ul>
      <li>Appetizers</li>
      <li>Main Courses</li>
      <li>Desserts</li>
      <li>Drinks</li>
    </ul>
  </div>

  <div id="about" class="content">
    <h2>About</h2>
    <p>Welcome to our restaurant! We pride ourselves on providing a memorable dining experience. Our team of talented chefs prepares the finest dishes using the freshest ingredients. Visit us to enjoy our warm hospitality and exceptional cuisine.</p>
  </div>
</body>
</html>

