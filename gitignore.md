<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="0 Infinity - A place for mysterious subjects and knowledge">
  <title>0 Infinity</title>
  <style>/* General Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Arial', sans-serif;
}

/* Body Styling */
body {
  background: #222222;
  color: #dcdcdc;
  font-family: 'Arial', sans-serif;
  line-height: 1.6;
  overflow-x: hidden;
}

/* Navbar Styling */
nav {
  position: fixed;
  top: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 30px;
  background-color: rgba(0, 0, 0, 0.85);
  z-index: 100;
  width: 100%;
  box-shadow: 0 4px 25px rgba(0, 0, 0, 0.5);
  transition: background-color 0.3s ease-in-out, transform 0.3s ease-in-out;
}

nav:hover {
  background-color: rgba(0, 0, 0, 1);
  transform: translateY(-3px);
}

.logo {
  display: flex;
  align-items: center;
}

.logo img {
  width: 40px;
}

.logo h2 {
  margin-left: 10px;
  color: #39ffde;
  font-size: 28px;
  letter-spacing: 2px;
  text-transform: uppercase;
  text-shadow: 0 0 8px rgba(0, 255, 255, 0.8);
}

.nav-links {
  display: flex;
  align-items: centre;
  list-style: none;
}

.nav-links a {
  display: block;
  padding: 20px 16px;
  color: #fff;
  text-decoration: none;
  font-size: 16px;
  text-transform: uppercase;
  transition: all 0.3s ease-in-out;
  letter-spacing: 1px;
}

.nav-links a:hover {
  background-color: #39ffde;
  color: #111;
  transform: translateY(-2px);
}

.nav-links .nav-cta-button {
  padding: 10px 18px;
  margin-left: 16px;
  border: 2px solid #39ffde;
  border-radius: 50px;
  color: #39ffde;
  font-weight: bold;
  transition: all 0.3s ease-in-out;
}

.nav-links .nav-cta-button:hover {
  background-color: #39ffde;
  color: #111;
  border: 2px solid #111;
  transform: scale(1.05);
}

/* Hamburger Icon Styles */
.hamburger {
  display: none;
  cursor: pointer;
  flex-direction: column;
  justify-content: space-between;
  height: 20px;
  width: 30px;
}

.hamburger .bar {
  height: 4px;
  width: 100%;
  background-color: #fff;
  transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out;
}

.hamburger.active .bar:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}

.hamburger.active .bar:nth-child(2) {
  opacity: 0;
}

.hamburger.active .bar:nth-child(3) {
  transform: rotate(-45deg) translate(5px, -5px);
}

/* Mobile Navigation Menu Styles */
.nav-links.open {
  display: block;
}

.nav-links li {
  text-align: center;
  margin: 10px 0;
}

.nav-links a {
  font-size: 18px;
}

.nav-links a:hover {
  background-color: #39ffde;
  transform: scale(1.05);
}

/* Hero Section Styling */
.hero {
  background: url('img/hero-background.jpg') no-repeat center center/cover;
  padding: 100px 20px;
  text-align: center;
  color: #dcdcdc;
  background-blend-mode: overlay;
  background-color: rgba(0, 0, 0, 0.6);
  transition: background-color 0.3s ease-in-out;
}

.hero:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

.hero-content h2 {
  font-size: 40px;
  margin-bottom: 20px;
  text-transform: uppercase;
  color: #39ffde;
  letter-spacing: 2px;
  text-shadow: 0 0 15px rgba(0, 255, 255, 0.8);
  animation: fadeInUp 1.5s ease-out;
}

.hero-content p {
  font-size: 20px;
  margin-bottom: 30px;
  color: #bbb;
  animation: fadeInUp 2s ease-out;
}

.cta-button {
  background-color: #39ffde;
  padding: 15px 30px;
  font-size: 18px;
  color: #111;
  text-decoration: none;
  border-radius: 50px;
  transition: background-color 0.3s ease, transform 0.3s ease;
}

.cta-button:hover {
  background-color: #32c8b8;
  transform: scale(1.1);
  box-shadow: 0 4px 20px rgba(0, 255, 255, 0.6);
}

/* Search Bar Styles */
.search-bar-container {
  display: flex;
  justify-content: center;
  padding: 20px;
}

.search-wrapper {
  position: relative;
  width: 80%;
}

.search-bar, .search-clear, .search-icon {
  font-size: 16px;
  border: 2px solid #333;
  border-radius: 25px;
  background-color: #333;
  color: #fff;
}

.search-bar {
  width: 100%;
  padding: 10px 20px;
  transition: all 0.3s ease-in-out;
}

.search-bar:focus {
  outline: none;
  border: 2px solid #39ffde;
}

.search-clear, .search-icon {
  position: absolute;
  top: 50px;
  right: 10px;
  background: none;
  border: none;
  font-size: 18px;
  cursor: pointer;
  color: #fff;
  transition: color 0.3s ease;
}

.search-clear:hover, .search-icon:hover {
  color: #39ffde;
}

/* Subjects Section Styling */
.subjects {
  padding: 10px 20px;
  background-color: #222;
  transition: background-color 0.3s ease-in-out;
}

.subjects:hover {
  background-color: #333;
}

.subjects h2 {
  text-align: center;
  font-size: 32px;
  margin-bottom: 40px;
  color: #39ffde;
  text-transform: uppercase;
  letter-spacing: 3px;
  animation: fadeInUp 1.5s ease-out;
}

.subject-cards {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}

.subject-card {
  background-color: #333;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 2px 15px rgba(0, 0, 0, 0.5);
  width: 250px;
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.subject-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.6);
}

.subject-card h3 {
  font-size: 24px;
  margin-bottom: 10px;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.subject-card p {
  font-size: 16px;
  color: #bbb;
}

/* Footer Section Styling */
footer {
  background-color: #111;
  color: #fff;
  text-align: center;
  padding: 20px 0;
  margin-top: 50px;
  animation: fadeInUp 2s ease-out;
}

footer p {
  font-size: 16px;
  color: #bbb;
}

/* Responsive Design */
@media (max-width: 768px) {
  nav {
    flex-wrap: wrap;
  }

  .hamburger {
    display: flex;
  }

  .nav-links {
    display: none;
    flex-basis: 100%;
    flex-wrap: wrap;
  }

  .nav-links li {
    flex-basis: 100%;
  }

  .nav-links a {
    text-align: center;
    font-size: 28px;
  }

  .nav-links .nav-cta-button {
    padding: 30px 16px;
    margin-left: 0;
    border: none;
    border-radius: 0;
    margin-bottom: 20px;
  }

  .subject-cards {
    display: flex;
    flex-direction: column;
  }

  .subject-card {
    margin: 10px 0;
    padding: 20px;
    background-color: #333;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
    transition: transform 0.3s ease-in-out;
  }

  .subject-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.6);
  }
}

/* Animation for elements */
@keyframes fadeInUp {
  0% {
    opacity: 0;
    transform: translateY(50px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Full-Screen Modal Styling */
#full-screen-modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
  display: none;
  justify-content: center;
  align-items: center;
}

#full-screen-modal .modal-content {
  background-color: #333;
  padding: 30px;
  position: relative;
  color: #fff;
  border-radius: 10px;
  box-shadow: 0 0 20px rgba(0, 255, 255, 0.5);
}

#close-modal {
  position: absolute;
  top: 10px;
  right: 10px;
  font-size: 20px;
  color: #39ffde;
  cursor: pointer;
  transition: color 0.3s ease;
}

#close-modal:hover {
  color: #fff;
}

/* ❞❝ मम समयं वृथा कर्तुं न रोचते। अहम् केवलं तान् एव इच्छामि ये व्यवसायिकाः सन्ति, स्वकार्ये तथा लक्ष्यम् प्रति समर्पिताः सन्ति। ❞❝ ⚡1%∞. . . */


   .subject {
      padding: 15px;
      margin-bottom: 15px;
      background-color: #007BFF;
      color: white;
      border-radius: 5px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
    }

   .subject:hover {
      background-color: #0056b3;
    }

   #overlay {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      color: white;
      z-index: 9999;
      padding: 20px;
      text-align: center;
    }

   button {
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      background-color: #bfbfbf;
      color: white;
      border-radius: 5px;
      cursor: pointer;
    }

   button:hover {
      background-color: #218838;
    }
/* ❞❝ मम समयं वृथा कर्तुं न रोचते। अहम् केवलं तान् एव इच्छामि ये व्यवसायिकाः सन्ति, स्वकार्ये तथा लक्ष्यम् प्रति समर्पिताः सन्ति। ❞❝ ⚡1%∞. . . */
</style>
</head>
<body>

  <!-- Navbar Section -->
  <header>
    <nav>
      <div class="logo">
        <img src="img/logo.png" alt="logo">
        <h2>0 Infinity ∞</h2>
      </div>
      <!-- Hamburger Icon for Mobile -->
      <div class="hamburger" id="hamburger-icon">
        <div class="bar"></div>
        <div class="bar"></div>
        <div class="bar"></div>
      </div>
      <!-- Navigation Links -->
      <ul class="nav-links" id="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#subjects">Subjects</a></li>
        <li><a href="#about">About Us</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#features">Features</a></li>
        <li><a href="#faqs">FAQs</a></li>
        <li><a class="nav-cta-button" href="#contact">Contact</a></li>
        <li><a href="#privacy">Privacy Policy</a></li>
        <li><a href="#feedback">Feedback</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h2>Explore the Mysteries of the World</h2>
      <p>Learn about mysterious subjects in simple words, with images, videos, and interactive content.</p>
      <a href="#subjects" class="cta-button">Start Exploring</a>
    </div>
  </section>

  <!-- Subjects Section -->
  <section id="subjects" class="subjects">
    <h2>Top Mysterious Subjects</h2>

    <!-- Search Bar Inside Subjects Section -->
  <div class="search-bar-container">
      <div class="search-wrapper">
        <input type="text" id="search-bar" class="search-bar" placeholder="Search Mystery" autocomplete="off">
        <button class="search-clear" id="clear-button" style="display:none;">×</button>
        <div id="suggestions" class="suggestions-list"></div>
        <button class="search-icon" id="search-icon">🔎</button>
      </div>
    </div>

    <!-- Subject Cards -->
  <div class="subject-cards">
      <div class="subject-card">
        <h3>Pyramids</h3>
        <p>The mysteries behind the ancient pyramids and their construction.</p>
      </div>
      <div class="subject-card">
        <h3>Aliens</h3>
        <p>Exploring theories and evidence of extraterrestrial life.</p>
      </div>
      <div class="subject-card">
        <h3>Time Travel</h3>
        <p>Theories and concepts about traveling through time.</p>
      </div>
      <div class="subject-card">
        <h3>Black Holes</h3>
        <p>Exploring the nature and mystery of black holes in space.</p>
      </div>
      <div class="subject-card">
        <h3>Ghosts</h3>
        <p>The supernatural and unexplained phenomena of ghosts.</p>
      </div>
      <div class="subject-card">
        <h3>Atlantis</h3>    <p>The mystery of the lost city of Atlantis.</p>
   </div>
   </div>
  </section>

  <!-- Modal Popup -->
  <div id="popup-modal" class="modal hidden">
    <div class="modal-content">
      <span class="close-button" id="close-modal">&times;</span<div class="search-bar-container">
      <div class="search-wrapper">
        <input type="text" id="search-bar" class="search-bar" placeholder="Search Mystery" autocomplete="off">
        <button class="search-clear" id="clear-button" style="display:none;">×</button>
        <div id="suggestions" class="suggestions-list"></div>
        <button class="search-icon" id="search-icon">🔎</button>
      </div>
    </div>

    <!-- Subject Cards -->
  <div class="subject-cards">
      <div class="subject-card">
        <h3>Pyramids</h3>
        <p>The mysteries behind the ancient pyramids and their construction.</p>
      </div>
      <div class="subject-card">
        <h3>Aliens</h3>
        <p>Exploring theories and evidence of extraterrestrial life.</p>
      </div>
      <div class="subject-card">
        <h3>Time Travel</h3>
        <p>Theories and concepts about traveling through time.</p>
      </div>
      <div class="subject-card">
        <h3>Black Holes</h3>
        <p>Exploring the nature and mystery of black holes in space.</p>
      </div>
      <div class="subject-card">
        <h3>Ghosts</h3>
        <p>The supernatural and unexplained phenomena of ghosts.</p>
      </div>
      <div class="subject-card">
        <h3>Atlantis</h3>
        <p>The mystery of the lost city of Atlantis.</p>
      </div>
    </div>
  </section>

  <!-- Modal Popup -->
  <div id="popup-modal" class="modal hidden">
    <div class="modal-content">
      <span class="close-button" id="close-modal">&times;</span>
      <div id="modal-body">

  <div id="modal-body">
        <!-- Dynamic Content will load here -->
      </div>
    </div>
  </div>

  <!-- Footer Section -->
  <footer id="contact">
    <p>© 2024 0 Infinity. All Rights Reserved.</p>
  </footer>

  <!-- Link to Script.js -->
  <script> document.addEventListener('DOMContentLoaded', () => {
  // Elements for Hamburger Menu
  const hamburgerIcon = document.getElementById('hamburger-icon');
  const navLinks = document.getElementById('nav-links');

  // Elements for Search Bar
  const searchInput = document.getElementById('search-bar');
  const clearButton = document.getElementById('clear-button');
  const suggestionsWrapper = document.getElementById('suggestions');
  const subjectCards = document.querySelector('.subject-cards');
  const subjectItems = document.querySelectorAll('.subject-card');

  // Elements for Modal Popup
  const modal = document.getElementById('popup-modal');
  const fullScreenModal = document.getElementById('full-screen-modal');
  const subjectNameElement = document.getElementById('subject-name');
  const closeModalButton = document.getElementById('close-modal');

  // Hamburger Menu Toggle
  hamburgerIcon.addEventListener('click', () => {
    navLinks.classList.toggle('open');
    hamburgerIcon.classList.toggle('active');
  });

  // Display suggestions based on search input
  searchInput.addEventListener('input', () => {
    const searchTerm = searchInput.value.trim().toLowerCase();
    if (searchTerm) {
      showSuggestions(searchTerm);
    } else {
      clearSuggestions();
    }
    toggleClearButtonVisibility();
  });

  // Show Suggestions
  const showSuggestions = (searchTerm) => {
    suggestionsWrapper.innerHTML = ''; // Clear previous suggestions
    const filteredItems = Array.from(subjectItems).filter(item => {
      const subjectName = item.querySelector('h3').textContent.toLowerCase();
      return subjectName.includes(searchTerm);
    });

    filteredItems.forEach(item => {
      const suggestionItem = document.createElement('div');
      suggestionItem.classList.add('suggestion-item');
      suggestionItem.textContent = item.querySelector('h3').textContent;

      suggestionItem.addEventListener('click', () => {
        searchInput.value = suggestionItem.textContent;
        clearSuggestions();
        moveSubjectToTop(item);
        openFullScreenModal(suggestionItem.textContent);
      });

      suggestionsWrapper.appendChild(suggestionItem);
    });

    suggestionsWrapper.style.display = filteredItems.length ? 'block' : 'none';
  };

  // Move selected subject to top
  const moveSubjectToTop = (item) => {
    subjectCards.prepend(item); // Prepend the selected item to the top of the container
  };

  // Clear suggestions
  const clearSuggestions = () => {
    suggestionsWrapper.innerHTML = '';
    suggestionsWrapper.style.display = 'none';
  };

  // Toggle visibility of clear button
  const toggleClearButtonVisibility = () => {
    clearButton.style.display = searchInput.value.trim() ? 'block' : 'none';
  };

  // Clear search input
  clearButton.addEventListener('click', () => {
    searchInput.value = '';
    clearButton.style.display = 'none';
    clearSuggestions();
  });

  // Open Full-Screen Modal with content
  const openFullScreenModal = (subjectName) => {
    subjectNameElement.textContent = subjectName; // Set the subject name in the modal

    // Show the modal
    fullScreenModal.classList.remove('hidden');
    fullScreenModal.style.display = 'flex'; // Ensure the modal is visible
  };

  // Close modal on button click
  closeModalButton.addEventListener('click', () => {
    fullScreenModal.classList.add('hidden');
    fullScreenModal.style.display = 'none'; // Hide the modal when closing
  });

  // Close modal when clicking outside the modal content
  fullScreenModal.addEventListener('click', (e) => {
    if (e.target === fullScreenModal) {
      fullScreenModal.classList.add('hidden');
      fullScreenModal.style.display = 'none';
    }
  });

  // Focus on search input when search icon is clicked
  const searchIcon = document.getElementById('search-icon');
  searchIcon.addEventListener('click', () => {
    searchInput.focus();
  });

  // Hide suggestions when clicking outside
  document.addEventListener('click', (event) => {
    if (!event.target.closest('.search-wrapper')) {
      clearSuggestions();
    }
  });
});</script>
</body>
</html>
