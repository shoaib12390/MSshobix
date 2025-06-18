<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Personal Portfolio</title>
    <!-- Chosen Palette: Clean & Modern Neutrals with a Fresh Accent (Background: #f9fafb, Text: #374151, Accent: #059669 - Emerald Green) -->
    <!-- Application Structure Plan: A single-page, vertical scrolling application with a sticky top navigation for easy anchoring to different sections: Home, About, Skills, Projects, and Contact. This structure is chosen for simplicity and quick access to all key information, ideal for a portfolio. Interactive elements like project filters and form validation enhance usability without adding unnecessary complexity. -->
    <!-- Visualization & Content Choices: Report Info: Personal Details, Skills, Projects -> Goal: Inform, Showcase -> Viz: Text blocks, icon lists, grid of project cards -> Interaction: Smooth scroll nav, project filtering buttons, simple form validation -> Justification: Clearly presents different types of information, allows easy navigation, and provides a clean, professional aesthetic for a portfolio. NO SVG/Mermaid used. All visual elements (icons, dividers) are created using Unicode characters, Tailwind CSS, or basic HTML elements. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f9fafb; /* Light background */
            color: #374151; /* Dark gray text */
        }
        .nav-link {
            transition: color 0.3s ease;
        }
        .nav-link:hover {
            color: #059669; /* Emerald Green on hover */
        }
        .section-heading {
            position: relative;
            display: inline-block;
        }
        .section-heading::after {
            content: '';
            position: absolute;
            width: 70%;
            height: 4px;
            background-color: #059669; /* Emerald Green underline */
            left: 15%;
            bottom: -8px;
            border-radius: 2px;
        }
        .project-card {
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0,0,0,0.1), 0 4px 6px -2px rgba(0,0,0,0.05);
        }
        .filter-button.active {
            background-color: #059669;
            color: white;
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800">

    <header class="bg-white/90 backdrop-blur-lg shadow-sm sticky top-0 z-50">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-gray-900">My Portfolio</a>
            <div class="hidden md:flex items-center space-x-8">
                <a href="#home" class="nav-link text-gray-600">Home</a>
                <a href="#about" class="nav-link text-gray-600">About</a>
                <a href="#skills" class="nav-link text-gray-600">Skills</a>
                <a href="#projects" class="nav-link text-gray-600">Projects</a>
                <a href="#contact" class="nav-link text-gray-600">Contact</a>
            </div>
            <button id="mobile-menu-button" class="md:hidden text-gray-600 focus:outline-none">
                ☰
            </button>
        </nav>
        <div id="mobile-menu" class="md:hidden bg-white shadow-lg hidden">
            <a href="#home" class="block px-6 py-3 text-gray-700 hover:bg-gray-100">Home</a>
            <a href="#about" class="block px-6 py-3 text-gray-700 hover:bg-gray-100">About</a>
            <a href="#skills" class="block px-6 py-3 text-gray-700 hover:bg-gray-100">Skills</a>
            <a href="#projects" class="block px-6 py-3 text-gray-700 hover:bg-gray-100">Projects</a>
            <a href="#contact" class="block px-6 py-3 text-gray-700 hover:bg-gray-100">Contact</a>
        </div>
    </header>

    <main class="container mx-auto px-6 py-12 md:py-20">

        <!-- Home Section -->
        <section id="home" class="flex flex-col md:flex-row items-center justify-center min-h-screen-75 text-center md:text-left mb-20 md:mb-32">
            <div class="md:w-1/2 mb-8 md:mb-0">
                <h1 class="text-5xl md:text-6xl font-bold text-gray-900 leading-tight mb-4">Hi, I'm [Your Name]</h1>
                <p class="text-xl md:text-2xl text-gray-600 mb-6">I'm a <span class="text-emerald-600 font-semibold">[Your Title, e.g., Frontend Developer, Data Analyst, UI/UX Designer]</span>.</p>
                <p class="text-lg text-gray-700 max-w-xl md:max-w-none mx-auto md:mx-0">
                    Welcome to my digital workspace, where I share my passion and expertise. Let's explore my work!
                </p>
                <a href="#projects" class="mt-8 inline-block bg-emerald-600 text-white font-semibold px-8 py-3 rounded-lg hover:bg-emerald-700 transition-colors shadow-md">
                    View My Projects
                </a>
            </div>
            <div class="md:w-1/2 flex justify-center md:justify-end">
                <!-- Placeholder for a personal image -->
                <img src="https://placehold.co/300x300/e2e8f0/64748b?text=Your%20Image" alt="Your Image" class="rounded-full shadow-lg border-4 border-white">
            </div>
        </section>

        <!-- About Section -->
        <section id="about" class="mb-20 md:mb-32">
            <h2 class="text-4xl font-bold text-center text-gray-900 mb-12 section-heading">About Me</h2>
            <div class="max-w-3xl mx-auto text-lg text-gray-700 leading-relaxed space-y-6">
                <p>
                    I am an [Your Expertise, e.g., experienced Frontend Developer] with a passion for crafting user-friendly and visually appealing web experiences. For [Number] years, I have worked on diverse projects in the [Industry or Field] sector, focusing on [Key Skills or Project Types].
                </p>
                <p>
                    My journey involves understanding data, designing beautiful interfaces, and transforming them into efficient code. I love solving complex problems and building innovative solutions that make a real impact. I am always eager to learn new technologies and best practices.
                </p>
                <p>
                    When I'm not coding or analyzing data, you can find me [Your Hobby, e.g., exploring new places, reading books, or spending time in nature].
                </p>
            </div>
        </section>

        <!-- Skills Section -->
        <section id="skills" class="mb-20 md:mb-32">
            <h2 class="text-4xl font-bold text-center text-gray-900 mb-12 section-heading">Skills</h2>
            <div class="max-w-4xl mx-auto grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6 text-center">
                <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
                    <div class="text-4xl mb-3">💻</div>
                    <h3 class="font-semibold text-xl text-gray-900">Frontend Development</h3>
                    <p class="text-sm text-gray-600">HTML, CSS, JavaScript, React.js, Tailwind CSS</p>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
                    <div class="text-4xl mb-3">📊</div>
                    <h3 class="font-semibold text-xl text-gray-900">Data Analysis</h3>
                    <p class="text-sm text-gray-600">Python (Pandas, NumPy), SQL, Tableau, Power BI</p>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
                    <div class="text-4xl mb-3">🎨</div>
                    <h3 class="font-semibold text-xl text-gray-900">UI/UX Design</h3>
                    <p class="text-sm text-gray-600">Figma, Adobe XD, Wireframing, Prototyping</p>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
                    <div class="text-4xl mb-3">🏗️</div>
                    <h3 class="font-semibold text-xl text-gray-900">Information Architecture</h3>
                    <p class="text-sm text-gray-600">User Flows, Sitemaps, Content Strategy</p>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
                    <div class="text-4xl mb-3">🌐</div>
                    <h3 class="font-semibold text-xl text-gray-900">Web Technologies</h3>
                    <p class="text-sm text-gray-600">RESTful APIs, Git, Responsive Design</p>
                </div>
                 <div class="bg-white p-6 rounded-lg shadow-sm border border-gray-200">
                    <div class="text-4xl mb-3">🧠</div>
                    <h3 class="font-semibold text-xl text-gray-900">Machine Learning (Basics)</h3>
                    <p class="text-sm text-gray-600">Scikit-learn, TensorFlow (Basics)</p>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects" class="mb-20 md:mb-32">
            <h2 class="text-4xl font-bold text-center text-gray-900 mb-12 section-heading">Projects</h2>
            <div class="flex justify-center space-x-4 mb-8">
                <button class="filter-button bg-gray-200 text-gray-700 px-4 py-2 rounded-full font-semibold hover:bg-gray-300 transition-colors active" data-filter="all">All</button>
                <button class="filter-button bg-gray-200 text-gray-700 px-4 py-2 rounded-full font-semibold hover:bg-gray-300 transition-colors" data-filter="web">Web Development</button>
                <button class="filter-button bg-gray-200 text-gray-700 px-4 py-2 rounded-full font-semibold hover:bg-gray-300 transition-colors" data-filter="data">Data Analysis</button>
                <button class="filter-button bg-gray-200 text-gray-700 px-4 py-2 rounded-full font-semibold hover:bg-gray-300 transition-colors" data-filter="design">UI/UX Design</button>
            </div>
            <div id="projects-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project Card 1 -->
                <div class="project-card bg-white p-6 rounded-lg shadow-md border border-gray-200" data-category="web">
                    <img src="https://placehold.co/400x250/d1fae5/059669?text=Website+Project+1" alt="Website Project 1" class="rounded-md mb-4 w-full">
                    <h3 class="font-bold text-xl text-gray-900 mb-2">E-commerce Redesign</h3>
                    <p class="text-gray-600 text-sm mb-4">Redesigned UI/UX and frontend for a faster, more user-friendly e-commerce website.</p>
                    <a href="#" target="_blank" class="text-emerald-600 hover:text-emerald-700 font-semibold text-sm">View Project »</a>
                </div>
                <!-- Project Card 2 -->
                <div class="project-card bg-white p-6 rounded-lg shadow-md border border-gray-200" data-category="data">
                    <img src="https://placehold.co/400x250/d1fae5/059669?text=Data+Project+1" alt="Data Project 1" class="rounded-md mb-4 w-full">
                    <h3 class="font-bold text-xl text-gray-900 mb-2">Sales Data Dashboard</h3>
                    <p class="text-gray-600 text-sm mb-4">Built an interactive dashboard to visualize sales trends and key performance indicators.</p>
                    <a href="#" target="_blank" class="text-emerald-600 hover:text-emerald-700 font-semibold text-sm">View Project »</a>
                </div>
                <!-- Project Card 3 -->
                <div class="project-card bg-white p-6 rounded-lg shadow-md border border-gray-200" data-category="design">
                    <img src="https://placehold.co/400x250/d1fae5/059669?text=App+UI+Project+1" alt="App UI Project 1" class="rounded-md mb-4 w-full">
                    <h3 class="font-bold text-xl text-gray-900 mb-2">Mobile App UI Concept</h3>
                    <p class="text-gray-600 text-sm mb-4">Complete UI/UX design flow for a fitness tracking mobile application.</p>
                    <a href="#" target="_blank" class="text-emerald-600 hover:text-emerald-700 font-semibold text-sm">View Project »</a>
                </div>
                <!-- Project Card 4 -->
                <div class="project-card bg-white p-6 rounded-lg shadow-md border border-gray-200" data-category="web">
                    <img src="https://placehold.co/400x250/d1fae5/059669?text=Website+Project+2" alt="Website Project 2" class="rounded-md mb-4 w-full">
                    <h3 class="font-bold text-xl text-gray-900 mb-2">Portfolio Website Template</h3>
                    <p class="text-gray-600 text-sm mb-4">Developed a customizable, responsive portfolio website template for creative professionals.</p>
                    <a href="#" target="_blank" class="text-emerald-600 hover:text-emerald-700 font-semibold text-sm">View Project »</a>
                </div>
                 <!-- Project Card 5 -->
                <div class="project-card bg-white p-6 rounded-lg shadow-md border border-gray-200" data-category="data">
                    <img src="https://placehold.co/400x250/d1fae5/059669?text=Data+Project+2" alt="Data Project 2" class="rounded-md mb-4 w-full">
                    <h3 class="font-bold text-xl text-gray-900 mb-2">Customer Segmentation Analysis</h3>
                    <p class="text-gray-600 text-sm mb-4">Derived insights using customer data for targeted marketing strategies.</p>
                    <a href="#" target="_blank" class="text-emerald-600 hover:text-emerald-700 font-semibold text-sm">View Project »</a>
                </div>
                <!-- Project Card 6 -->
                <div class="project-card bg-white p-6 rounded-lg shadow-md border border-gray-200" data-category="design">
                    <img src="https://placehold.co/400x250/d1fae5/059669?text=Website+UI+Project+2" alt="Website UI Project 2" class="rounded-md mb-4 w-full">
                    <h3 class="font-bold text-xl text-gray-900 mb-2">SaaS Dashboard UX Improvement</h3>
                    <p class="text-gray-600 text-sm mb-4">Streamlined user experience flows and interfaces for a SaaS product.</p>
                    <a href="#" target="_blank" class="text-emerald-600 hover:text-emerald-700 font-semibold text-sm">View Project »</a>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="mb-20">
            <h2 class="text-4xl font-bold text-center text-gray-900 mb-12 section-heading">Contact</h2>
            <div class="max-w-xl mx-auto bg-white p-8 rounded-lg shadow-md border border-gray-200">
                <p class="text-center text-gray-600 mb-6">Have a project you'd like to discuss? Or just want to say hello?</p>
                <form id="contact-form" class="space-y-4">
                    <div>
                        <label for="name" class="block text-gray-700 text-sm font-semibold mb-2">Your Name:</label>
                        <input type="text" id="name" name="name" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-emerald-500" required>
                    </div>
                    <div>
                        <label for="email" class="block text-gray-700 text-sm font-semibold mb-2">Your Email:</label>
                        <input type="email" id="email" name="email" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-emerald-500" required>
                    </div>
                    <div>
                        <label for="message" class="block text-gray-700 text-sm font-semibold mb-2">Your Message:</label>
                        <textarea id="message" name="message" rows="5" class="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-emerald-500" required></textarea>
                    </div>
                    <button type="submit" class="w-full bg-emerald-600 text-white font-semibold px-6 py-3 rounded-lg hover:bg-emerald-700 transition-colors shadow-md">Send Message</button>
                    <div id="form-message" class="mt-4 text-center text-sm font-medium hidden"></div>
                </form>
            </div>
        </section>

    </main>

    <footer class="bg-gray-900 text-gray-400 mt-20">
        <div class="container mx-auto px-6 py-8 text-center">
            <p>&copy; 2025 [Your Name]. All rights reserved.</p>
            <p class="text-sm mt-2">Crafted by a passionate developer.</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // Smooth scrolling for navigation links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    document.querySelector(this.getAttribute('href')).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });

            // Mobile menu toggle
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            mobileMenuButton.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });

            // Project filtering
            const filterButtons = document.querySelectorAll('.filter-button');
            const projectsGrid = document.getElementById('projects-grid');
            const projectCards = document.querySelectorAll('.project-card');

            filterButtons.forEach(button => {
                button.addEventListener('click', () => {
                    // Remove active class from all buttons
                    filterButtons.forEach(btn => btn.classList.remove('active'));
                    // Add active class to clicked button
                    button.classList.add('active');

                    const filter = button.dataset.filter;

                    projectCards.forEach(card => {
                        const category = card.dataset.category;
                        if (filter === 'all' || category === filter) {
                            card.style.display = 'block'; /* Show the card */
                        } else {
                            card.style.display = 'none'; /* Hide the card */
                        }
                    });
                });
            });

            // Contact form submission (client-side simulation)
            const contactForm = document.getElementById('contact-form');
            const formMessage = document.getElementById('form-message');

            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();

                const name = document.getElementById('name').value;
                const email = document.getElementById('email').value;
                const message = document.getElementById('message').value;

                if (name && email && message) {
                    formMessage.classList.remove('hidden', 'text-red-500');
                    formMessage.classList.add('text-green-500');
                    formMessage.textContent = 'Your message has been sent successfully! We will get back to you shortly.';
                    contactForm.reset(); // Clear the form
                } else {
                    formMessage.classList.remove('hidden', 'text-green-500');
                    formMessage.classList.add('text-red-500');
                    formMessage.textContent = 'Please fill out all fields.';
                }
                formMessage.style.display = 'block'; // Ensure message is visible
            });
        });
    </script>
</body>
</html>
