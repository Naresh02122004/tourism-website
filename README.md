<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tourism Website</title>
    <style>
        /* General Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Body Style */
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            min-height: 100vh;
            background: linear-gradient(90deg, blue, red);
            color: white;
            padding-top: 60px;
        }

        /* Welcome Page */
        .welcome-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 90vh;
        }

        h1 {
            font-size: 4rem;
            font-weight: bold;
            margin-bottom: 20px;
        }

        .image-label {
            font-size: 1.5rem;
            font-weight: bold;
            color: white;
        }

        /* Button */
        .button {
            margin-top: 20px;
            padding: 12px 24px;
            font-size: 1.2rem;
            font-weight: bold;
            color: white;
            background-color: rgba(0, 0, 0, 0.7);
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: background 0.3s, transform 0.2s;
        }

        .button:hover {
            background-color: rgba(255, 255, 255, 0.3);
            transform: scale(1.1);
        }

        /* Second Page Content */
        .secondPage {
            display: none;
            width: 80%;
            margin: auto;
            text-align: left;
            margin-top: 40px;
            background-color: #f0f0f0;
            color: black;
        }

        h2 {
            margin-top: 20px;
        }

        ul {
            list-style-type: disc;
            margin-left: 20px;
        }

        /* Second Page Navigation - Top Right */
        .secondPage nav {
            position: fixed;
            top: 15px;
            right: 15px;
            text-align: right;
            background: rgba(0, 0, 0, 0.7);
            padding: 10px;
            border-radius: 5px;
        }

        .secondPage nav a {
            text-decoration: none;
            color: white;
            font-size: 1.2rem;
            margin: 0 15px;
            font-weight: bold;
        }

        .secondPage nav a:hover {
            color: yellow;
        }

        /* Places Section */
        .places-section {
            display: none;
            margin-top: 40px;
            background-color: #f4f4f4; /* Light gray background for places section */
            padding: 20px;
            color: black;
        }

        .place {
            margin-bottom: 30px;
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            color: black;
        }

        .place img {
            max-width: 100%;
            height: auto;
            border-radius: 5px;
        }

        /* About Section */
        .about-section {
            display: block;
        }

        /* Login Section */
        .login-section {
            display: none;
            background-color: white;
            color: black;
            padding: 20px;
            border-radius: 10px;
            width: 100%;
            max-width: 400px;
            margin: 0 auto;
            text-align: left;
        }

        .login-section h2 {
            margin-bottom: 20px;
        }

        .login-section input {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            border-radius: 5px;
            border: 1px solid #ccc;
            font-size: 1rem;
        }

        .login-section button {
            width: 100%;
            padding: 12px;
            background-color: blue;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1.2rem;
            cursor: pointer;
            margin-bottom: 10px;
        }

        .login-section button:hover {
            background-color: darkblue;
        }

        .login-section .google-signin {
            width: 100%;
            padding: 12px;
            background-color: #db4437;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1.2rem;
            cursor: pointer;
            margin-bottom: 10px;
        }

        .login-section .google-signin:hover {
            background-color: darkred;
        }

        .login-section .signup {
            text-align: center;
        }

        .login-section .signup a {
            text-decoration: none;
            color: blue;
            font-size: 1.1rem;
        }

        .login-section .signup a:hover {
            text-decoration: underline;
        }

    </style>
</head>
<body>

    <!-- Welcome Page -->
    <div class="welcome-container" id="welcomePage">
        <h1>Welcome</h1>
        <div class="image-label">TOURISM</div>
        <button class="button" onclick="showSecondPage()">Next</button>
    </div>

    <!-- Second Page Content -->
    <div class="secondPage" id="secondPage">
        <!-- Second Page Navigation -->
        <nav>
            <a href="#" onclick="showWelcomePage()">Home</a>
            <a href="#" onclick="showAboutSection()">About</a>
            <a href="#" onclick="showPlacesSection()">Places</a>
            <a href="#" onclick="showLoginSection()">Login</a>
        </nav>

        <!-- Introduction Section -->
        <div id="introduction" class="about-section">
            <h1>Introduction</h1>
            <p>Tourism involves the movement of people to places outside their usual environment for various purposes, primarily leisure, recreation, and pleasure.</p>
            <p>Tourism is a multifaceted phenomenon that involves the movement of people to countries or places outside their usual environment for personal, business, or professional purposes. This movement typically involves travel for leisure, recreation, and pleasure, but can also encompass business trips, visiting friends and relatives, education, and health-related purposes.</p>
        </div>

        <!-- Key Components Section -->
        <div id="keyComponents" class="about-section">
            <h2>Key Components</h2>
            <ul>
                <li><strong>Travel:</strong> The act of moving from one place to another.</li>
                <li><strong>Stay:</strong> Temporary residence in a destination.</li>
                <li><strong>Purpose:</strong> Diverse reasons for travel, including leisure, business, and personal.</li>
            </ul>
        </div>

        <!-- Economic Impact Section -->
        <div id="economicImpact" class="about-section">
            <h2>Economic Impact</h2>
            <ul>
                <li><strong>Job creation:</strong> Tourism supports numerous jobs in sectors like hospitality, transportation, and retail.</li>
                <li><strong>Revenue generation:</strong> Generates significant income for countries and regions.</li>
                <li><strong>Economic development:</strong> Contributes to infrastructure development and local economic growth.</li>
            </ul>
        </div>

        <!-- Environmental Impact Section -->
        <div id="environmentalImpact" class="about-section">
            <h2>Environmental Impact</h2>
            <ul>
                <li><strong>Positive:</strong> Can raise awareness about environmental conservation.</li>
                <li><strong>Negative:</strong> Can contribute to environmental degradation, such as pollution and resource depletion.</li>
            </ul>
        </div>
    </div>

    <!-- Login Section -->
    <div class="login-section" id="loginSection">
        <h2>Login</h2>
        <input type="text" placeholder="Enter Name" id="name" />
        <input type="tel" placeholder="Enter Phone Number" id="phone" />
        <button>Sign In</button>
        <button class="google-signin">Sign in with Google</button>
        <div class="signup">
            <p>Don't have an account? <a href="#">Sign up</a></p>
        </div>
    </div>

    <!-- Historical Places Section -->
    <div class="places-section" id="placesSection">
        <h1>Historical Places in Andhra Pradesh</h1>
        
        <!-- Place 1 -->
        <div class="place">
            <h2>Chilkur Balaji Temple</h2>
            <img src="https://upload.wikimedia.org/wikipedia/commons/c/c7/Chilkur_Balaji_Temple.jpg" alt="Chilkur Balaji Temple">
            <p><strong>Address:</strong> Chilkur, Hyderabad, Andhra Pradesh, India</p>
            <p><strong>Pincode:</strong> 500075</p>
        </div>
        <!-- Place 2 -->
        <div class="place">
            <h3>Simhachalam Temple</h3>
            <img src="https://upload.wikimedia.org/wikipedia/commons/7/7d/Simhachalam_Temple.jpg" alt="Simhachalam Temple">
            <p>Address: Visakhapatnam, Andhra Pradesh</p>
        </div>
<!-- Place 3 -->
        <div class="place">
            <h2>Srivari Temple, Tirupati</h2>
            <img src="https://upload.wikimedia.org/wikipedia/commons/c/cd/Tirumala_Temple.jpg" alt="Tirupati Temple">
            <p><strong>Address:</strong> Tirumala, Tirupati, Andhra Pradesh, India</p>
            <p><strong>Pincode:</strong> 517504</p>
        </div>
  <!-- Place 4 -->
<div class="place">
                <h2>Kanaka Durga Temple</h2>
                <img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/Kanaka_Durga_Temple.jpg" alt="Kanaka Durga Temple">
                <p>Address: Vijayawada, Andhra Pradesh</p>
            </div>
  <!-- Place 5 -->
        <div class="place">
            <h3>Amaravati Stupa</h3>
            <img src="https://upload.wikimedia.org/wikipedia/commons/5/5a/Amaravati_Buddhist_Stupa_3.jpg" alt="Amaravati Stupa">
            <p>Address: Amaravati, Guntur, Andhra Pradesh</p>
        </div>
  <!-- Place 6 -->
<div class="place">
            <h2>Vijayanagar Fort</h2>
            <img src="https://upload.wikimedia.org/wikipedia/commons/4/47/Vijayanagar_Fort.jpg" alt="Vijayanagar Fort">
            <p><strong>Address:</strong> Vijayanagar, Anantapur, Andhra Pradesh, India</p>
            <p><strong>Pincode:</strong> 515001</p>
        </div>

        <!-- Place 7 -->
        <div class="place">
            <h2>Vijayanagar Fort</h2>
            <img src="https://upload.wikimedia.org/wikipedia/commons/4/47/Vijayanagar_Fort.jpg" alt="Vijayanagar Fort">
            <p><strong>Address:</strong> Vijayanagar, Anantapur, Andhra Pradesh, India</p>
            <p><strong>Pincode:</strong> 515001</p>
        </div>
          <!-- Place 8 -->
        <div class="section" id="beaches">
            <h2>Beaches</h2>
            <div class="place">
                <h3>Rishikonda Beach</h3>
                <img src="https://upload.wikimedia.org/wikipedia/commons/3/3b/Rishikonda_Beach.jpg" alt="Rishikonda Beach">
                <p>Address: Visakhapatnam, Andhra Pradesh</p>
            </div>
             <!-- Place 9 -->
            <div class="place">
                <h3>Yarada Beach</h3>
                <img src="https://upload.wikimedia.org/wikipedia/commons/2/2b/Yarada_Beach.jpg" alt="Yarada Beach">
                <p>Address: Visakhapatnam, Andhra Pradesh</p>
            </div>
  <!-- Place 10 -->
<div class="place">
            <h3>Ramakrishna Beach</h3>
            <img src="https://upload.wikimedia.org/wikipedia/commons/4/48/Ramakrishna_Beach_Visakhapatnam.jpg" alt="Ramakrishna Beach">
            <p>Address: Visakhapatnam, Andhra Pradesh</p>
        </div>

    
    </div>

    <script>
        function showSecondPage() {
            document.getElementById('welcomePage').style.display = 'none';
            document.getElementById('secondPage').style.display = 'block';
        }

        function showWelcomePage() {
            document.getElementById('welcomePage').style.display = 'flex';
            document.getElementById('secondPage').style.display = 'none';
            document.getElementById('placesSection').style.display = 'none';
            document.getElementById('loginSection').style.display = 'none';
        }

        function showAboutSection() {
            const sections = document.querySelectorAll('.about-section');
            sections.forEach(function(section) {
                section.style.display = 'block';
            });
            document.getElementById('placesSection').style.display = 'none';
            document.getElementById('loginSection').style.display = 'none';
        }

        function showPlacesSection() {
            document.getElementById('placesSection').style.display = 'block';
            document.querySelectorAll('.about-section').forEach(function(section) {
                section.style.display = 'none';
            });
            document.getElementById('loginSection').style.display = 'none';
        }

        function showLoginSection() {
            document.getElementById('loginSection').style.display = 'block';
            document.getElementById('secondPage').style.display = 'none';
            document.getElementById('placesSection').style.display = 'none';
        }
    </script>

</body>
</html>
