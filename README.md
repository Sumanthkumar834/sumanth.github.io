<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sumanth Medaramettala | Data Scientist</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        primary: {
                            50: '#f5f3ff',
                            100: '#ede9fe',
                            200: '#ddd6fe',
                            300: '#c4b5fd',
                            400: '#a78bfa',
                            500: '#8b5cf6',
                            600: '#7c3aed',
                            700: '#6d28d9',
                            800: '#5b21b6',
                            900: '#4c1d95',
                        }
                    }
                }
            }
        }
    </script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .gradient-bg {
            background: linear-gradient(135deg, #4f46e5 0%, #7c3aed 50%, #9333ea 100%);
        }
        .dark .gradient-bg {
            background: linear-gradient(135deg, #3730a3 0%, #5b21b6 50%, #6d28d9 100%);
        }
        .project-card {
            transition: all 0.3s ease;
        }
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        .dark .project-card:hover {
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.25), 0 10px 10px -5px rgba(0, 0, 0, 0.1);
        }
        .skill-bar {
            height: 8px;
            border-radius: 4px;
        }
        .timeline-item:not(:last-child)::after {
            content: '';
            position: absolute;
            left: 18px;
            top: 30px;
            height: calc(100% - 30px);
            width: 2px;
            background: #e5e7eb;
        }
        .dark .timeline-item:not(:last-child)::after {
            background: #374151;
        }
        .tool-icon {
            transition: all 0.3s ease;
        }
        .tool-icon:hover {
            transform: scale(1.1);
        }
        .animate-fadeIn {
            animation: fadeIn 0.5s ease forwards;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .theme-toggle {
            transition: all 0.3s ease;
        }
        .theme-toggle:hover {
            transform: rotate(30deg);
        }
    </style>
</head>
<body class="font-sans bg-gray-50 text-gray-800 dark:bg-gray-900 dark:text-gray-100 transition-colors duration-300">
    <!-- Navigation -->
    <nav class="bg-white dark:bg-gray-800 shadow-sm fixed w-full z-10">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <span class="text-xl font-bold text-primary-600 dark:text-primary-400">SM</span>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="#about" class="text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 transition">About</a>
                    <a href="#experience" class="text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 transition">Experience</a>
                    <a href="#projects" class="text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 transition">Projects</a>
                    <a href="#skills" class="text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 transition">Skills</a>
                    <a href="#education" class="text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 transition">Education</a>
                    <a href="#contact" class="text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 transition">Contact</a>
                    <button id="theme-toggle" class="theme-toggle text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 p-2 rounded-full focus:outline-none">
                        <i class="fas fa-moon dark:hidden"></i>
                        <i class="fas fa-sun hidden dark:block"></i>
                    </button>
                </div>
                <div class="md:hidden flex items-center space-x-4">
                    <button id="theme-toggle-mobile" class="theme-toggle text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 p-2 rounded-full focus:outline-none">
                        <i class="fas fa-moon dark:hidden"></i>
                        <i class="fas fa-sun hidden dark:block"></i>
                    </button>
                    <button class="text-gray-700 dark:text-gray-300" id="menu-toggle">
                        <i class="fas fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>
        <!-- Mobile menu -->
        <div class="md:hidden hidden bg-white dark:bg-gray-800 py-2 px-4 shadow-lg" id="mobile-menu">
            <a href="#about" class="block py-2 text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 transition">About</a>
            <a href="#experience" class="block py-2 text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 transition">Experience</a>
            <a href="#projects" class="block py-2 text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 transition">Projects</a>
            <a href="#skills" class="block py-2 text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 transition">Skills</a>
            <a href="#education" class="block py-2 text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 transition">Education</a>
            <a href="#contact" class="block py-2 text-gray-700 dark:text-gray-300 hover:text-primary-600 dark:hover:text-primary-400 transition">Contact</a>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="gradient-bg text-white pt-32 pb-20">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-10 md:mb-0">
                    <h1 class="text-4xl md:text-5xl font-bold mb-4">Sumanth Medaramettala</h1>
                    <h2 class="text-2xl md:text-3xl font-semibold mb-6">Data Scientist & AI Engineer</h2>
                    <p class="text-lg mb-8 opacity-90">Transforming complex data into actionable insights with expertise in machine learning, deep learning, and data engineering. Published researcher with patents in AI applications.</p>
                    <div class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4">
                        <a href="#contact" class="bg-white text-primary-600 px-6 py-3 rounded-lg font-medium hover:bg-gray-100 transition text-center">Contact Me</a>
                        <a href="#" class="border border-white text-white px-6 py-3 rounded-lg font-medium hover:bg-white hover:bg-opacity-10 transition text-center">Download CV</a>
                    </div>
                </div>
                <div class="md:w-1/2 flex justify-center">
                    <div class="relative">
                        <div class="w-64 h-64 md:w-80 md:h-80 bg-white bg-opacity-20 rounded-full absolute -inset-2 animate-pulse"></div>
                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80" 
                             alt="Sumanth Medaramettala" 
                             class="w-64 h-64 md:w-80 md:h-80 rounded-full object-cover relative z-10 border-4 border-white">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 bg-white dark:bg-gray-800">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-3xl font-bold text-center mb-16">About Me</h2>
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/3 mb-10 md:mb-0 flex justify-center">
                    <img src="https://images.unsplash.com/photo-1571171637578-41bc2dd41cd2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80" 
                         alt="Working" 
                         class="rounded-lg shadow-lg w-full max-w-md dark:shadow-gray-700">
                </div>
                <div class="md:w-2/3 md:pl-12">
                    <p class="text-lg mb-6">
                        I'm a passionate Data Scientist and AI Engineer with experience in extracting meaningful insights from complex datasets. 
                        My expertise lies in developing machine learning models, deep learning architectures, and implementing data-driven solutions.
                    </p>
                    <p class="text-lg mb-6">
                        Currently pursuing my Master's in Computer Science at University of South Florida with a focus on AI and Trustworthy Computing. 
                        My approach combines technical expertise with research acumen to deliver impactful results.
                    </p>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 mt-8">
                        <div class="flex items-center bg-gray-50 dark:bg-gray-700 p-4 rounded-lg">
                            <div class="bg-primary-100 dark:bg-primary-900 p-3 rounded-full mr-4">
                                <i class="fas fa-graduation-cap text-primary-600 dark:text-primary-300"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold">Education</h4>
                                <p class="text-gray-600 dark:text-gray-300">MS Computer Science</p>
                            </div>
                        </div>
                        <div class="flex items-center bg-gray-50 dark:bg-gray-700 p-4 rounded-lg">
                            <div class="bg-primary-100 dark:bg-primary-900 p-3 rounded-full mr-4">
                                <i class="fas fa-briefcase text-primary-600 dark:text-primary-300"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold">Experience</h4>
                                <p class="text-gray-600 dark:text-gray-300">3+ Years</p>
                            </div>
                        </div>
                        <div class="flex items-center bg-gray-50 dark:bg-gray-700 p-4 rounded-lg">
                            <div class="bg-primary-100 dark:bg-primary-900 p-3 rounded-full mr-4">
                                <i class="fas fa-project-diagram text-primary-600 dark:text-primary-300"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold">Projects</h4>
                                <p class="text-gray-600 dark:text-gray-300">10+ Completed</p>
                            </div>
                        </div>
                        <div class="flex items-center bg-gray-50 dark:bg-gray-700 p-4 rounded-lg">
                            <div class="bg-primary-100 dark:bg-primary-900 p-3 rounded-full mr-4">
                                <i class="fas fa-trophy text-primary-600 dark:text-primary-300"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold">Certifications</h4>
                                <p class="text-gray-600 dark:text-gray-300">Azure, Google Analytics</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="py-20 bg-gray-50 dark:bg-gray-800">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-3xl font-bold text-center mb-16">My Experience</h2>
            <div class="relative">
                <!-- Timeline -->
                <div class="space-y-8">
                    <!-- Item 1 -->
                    <div class="timeline-item relative pl-12">
                        <div class="absolute left-0 top-0 w-8 h-8 bg-primary-600 rounded-full flex items-center justify-center text-white">
                            <i class="fas fa-briefcase"></i>
                        </div>
                        <div class="bg-white dark:bg-gray-700 p-6 rounded-lg shadow-sm">
                            <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-4">
                                <h3 class="text-xl font-semibold">Data Analyst</h3>
                                <span class="text-primary-600 dark:text-primary-400 font-medium">Mar 2021 - Jul 2022</span>
                            </div>
                            <h4 class="text-lg font-medium text-gray-700 dark:text-gray-300 mb-3">Cognizant Technology Solutions, Bangalore, India</h4>
                            <p class="text-gray-600 dark:text-gray-300">
                                • Collected, cleaned, and structured 1M+ data points from multiple sources using SQL, Python (Pandas, NumPy), improving data integrity by 20%<br>
                                • Designed and optimized relational databases (MySQL, PostgreSQL), reducing query execution time by 30%<br>
                                • Applied predictive analytics and regression models in Python to uncover customer behavior trends, leading to a 15% increase in targeted marketing effectiveness<br>
                                • Built automated ETL pipelines using Python (Pandas, SQLAlchemy), reducing manual reporting time by 40%<br>
                                • Conducted real-time performance monitoring of data systems, reducing downtime by 25%
                            </p>
                        </div>
                    </div>
                    
                    <!-- Item 2 -->
                    <div class="timeline-item relative pl-12">
                        <div class="absolute left-0 top-0 w-8 h-8 bg-primary-600 rounded-full flex items-center justify-center text-white">
                            <i class="fas fa-briefcase"></i>
                        </div>
                        <div class="bg-white dark:bg-gray-700 p-6 rounded-lg shadow-sm">
                            <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-4">
                                <h3 class="text-xl font-semibold">Data Analyst Intern</h3>
                                <span class="text-primary-600 dark:text-primary-400 font-medium">Sep 2020 - Feb 2021</span>
                            </div>
                            <h4 class="text-lg font-medium text-gray-700 dark:text-gray-300 mb-3">InsightIQ Analytics, Bangalore, India</h4>
                            <p class="text-gray-600 dark:text-gray-300">
                                • Collected, cleaned, and analyzed product and user data using SQL and Python to uncover insights that shaped product decisions<br>
                                • Designed automated reporting dashboards in Excel and PowerBI to track key performance metrics<br>
                                • Worked closely with the founding team to support MVP development through data-driven feature validation<br>
                                • Contributed to sprint planning and client demo sessions in fast-paced startup environments
                            </p>
                        </div>
                    </div>
                    
                    <!-- Item 3 -->
                    <div class="timeline-item relative pl-12">
                        <div class="absolute left-0 top-0 w-8 h-8 bg-primary-600 rounded-full flex items-center justify-center text-white">
                            <i class="fas fa-chart-line"></i>
                        </div>
                        <div class="bg-white dark:bg-gray-700 p-6 rounded-lg shadow-sm">
                            <div class="flex flex-col md:flex-row md:justify-between md:items-center mb-4">
                                <h3 class="text-xl font-semibold">Concession Operations Analyst</h3>
                                <span class="text-primary-600 dark:text-primary-400 font-medium">Sep 2023 - Present</span>
                            </div>
                            <h4 class="text-lg font-medium text-gray-700 dark:text-gray-300 mb-3">Yuengling Center, University of South Florida, Tampa, FL</h4>
                            <p class="text-gray-600 dark:text-gray-300">
                                • Analyze weekly sales data and generate reports on inventory, demand trends, and restocking using Excel and POS systems<br>
                                • Led teams across multiple stands during major events, improving efficiency and real-time operations
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-20 bg-white dark:bg-gray-800">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-3xl font-bold text-center mb-16">Featured Projects</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project 1 -->
                <div class="project-card bg-white dark:bg-gray-700 rounded-xl shadow-md overflow-hidden transition duration-300">
                    <div class="h-48 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                             alt="Music Genre Classification" 
                             class="w-full h-full object-cover">
                    </div>
                    <div class="p-6">
                        <div class="flex items-center mb-2">
                            <span class="bg-primary-100 dark:bg-primary-900 text-primary-600 dark:text-primary-300 text-xs font-semibold px-3 py-1 rounded-full">Deep Learning</span>
                            <span class="bg-green-100 dark:bg-green-900 text-green-600 dark:text-green-300 text-xs font-semibold px-3 py-1 rounded-full ml-2">TensorFlow</span>
                        </div>
                        <h3 class="text-xl font-bold mb-2 dark:text-white">Trustworthy Music Genre Classification</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">
                            Achieved 85% accuracy with VGG16 & ResNet using transfer learning on GTZAN dataset. Integrated SHAP for explainability and fairness evaluation.
                        </p>
                        <div class="flex justify-between items-center">
                            <a href="#" class="text-primary-600 dark:text-primary-400 font-medium hover:text-primary-800 dark:hover:text-primary-300">View Details →</a>
                            <div class="flex space-x-2">
                                <a href="#" class="text-gray-500 dark:text-gray-400 hover:text-gray-700 dark:hover:text-gray-200"><i class="fab fa-github"></i></a>
                                <a href="#" class="text-gray-500 dark:text-gray-400 hover:text-gray-700 dark:hover:text-gray-200"><i class="fas fa-external-link-alt"></i></a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="project-card bg-white dark:bg-gray-700 rounded-xl shadow-md overflow-hidden transition duration-300">
                    <div class="h-48 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1620712943543-bcc4688e7485?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                             alt="Facial Emotion Recognition" 
                             class="w-full h-full object-cover">
                    </div>
                    <div class="p-6">
                        <div class="flex items-center mb-2">
                            <span class="bg-blue-100 dark:bg-blue-900 text-blue-600 dark:text-blue-300 text-xs font-semibold px-3 py-1 rounded-full">CNN</span>
                            <span class="bg-yellow-100 dark:bg-yellow-900 text-yellow-600 dark:text-yellow-300 text-xs font-semibold px-3 py-1 rounded-full ml-2">OpenCV</span>
                        </div>
                        <h3 class="text-xl font-bold mb-2 dark:text-white">Facial Emotion Recognition</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">
                            Developed CNN model using Python, TensorFlow, and OpenCV achieving 92% accuracy on CK+ dataset. Published in SCOPUS Journal with Australian patent.
                        </p>
                        <div class="flex justify-between items-center">
                            <a href="#" class="text-primary-600 dark:text-primary-400 font-medium hover:text-primary-800 dark:hover:text-primary-300">View Details →</a>
                            <div class="flex space-x-2">
                                <a href="#" class="text-gray-500 dark:text-gray-400 hover:text-gray-700 dark:hover:text-gray-200"><i class="fab fa-github"></i></a>
                                <a href="#" class="text-gray-500 dark:text-gray-400 hover:text-gray-700 dark:hover:text-gray-200"><i class="fas fa-external-link-alt"></i></a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="project-card bg-white dark:bg-gray-700 rounded-xl shadow-md overflow-hidden transition duration-300">
                    <div class="h-48 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                             alt="Voice Controlled Robot" 
                             class="w-full h-full object-cover">
                    </div>
                    <div class="p-6">
                        <div class="flex items-center mb-2">
                            <span class="bg-red-100 dark:bg-red-900 text-red-600 dark:text-red-300 text-xs font-semibold px-3 py-1 rounded-full">IoT</span>
                            <span class="bg-purple-100 dark:bg-purple-900 text-purple-600 dark:text-purple-300 text-xs font-semibold px-3 py-1 rounded-full ml-2">Raspberry Pi</span>
                        </div>
                        <h3 class="text-xl font-bold mb-2 dark:text-white">Voice Controlled Robotic Vehicle</h3>
                        <p class="text-gray-600 dark:text-gray-300 mb-4">
                            Built using Raspberry Pi, Python, OpenCV, and ultrasonic sensors enabling hands-free navigation. Research published in IJARCS (2020).
                        </p>
                        <div class="flex justify-between items-center">
                            <a href="#" class="text-primary-600 dark:text-primary-400 font-medium hover:text-primary-800 dark:hover:text-primary-300">View Details →</a>
                            <div class="flex space-x-2">
                                <a href="#" class="text-gray-500 dark:text-gray-400 hover:text-gray-700 dark:hover:text-gray-200"><i class="fab fa-github"></i></a>
                                <a href="#" class="text-gray-500 dark:text-gray-400 hover:text-gray-700 dark:hover:text-gray-200"><i class="fas fa-external-link-alt"></i></a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="text-center mt-12">
                <a href="#" class="inline-flex items-center px-6 py-3 border border-primary-600 text-primary-600 dark:border-primary-400 dark:text-primary-400 rounded-lg hover:bg-primary-50 dark:hover:bg-gray-700 transition">
                    View All Projects <i class="fas fa-arrow-right ml-2"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-20 bg-gray-50 dark:bg-gray-800">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-3xl font-bold text-center mb-16">My Skills</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                <!-- Technical Skills -->
                <div>
                    <h3 class="text-xl font-semibold mb-6 flex items-center">
                        <i class="fas fa-code text-primary-600 dark:text-primary-400 mr-3"></i> Technical Skills
                    </h3>
                    <div class="space-y-6">
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="font-medium">Python (Pandas, NumPy, Scikit-learn)</span>
                                <span class="text-gray-600 dark:text-gray-300">Expert</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="skill-bar bg-primary-600 h-2.5 rounded-full" style="width: 95%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="font-medium">SQL</span>
                                <span class="text-gray-600 dark:text-gray-300">Advanced</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="skill-bar bg-primary-600 h-2.5 rounded-full" style="width: 90%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="font-medium">Machine Learning</span>
                                <span class="text-gray-600 dark:text-gray-300">Expert</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="skill-bar bg-primary-600 h-2.5 rounded-full" style="width: 92%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="font-medium">Deep Learning (TensorFlow, PyTorch)</span>
                                <span class="text-gray-600 dark:text-gray-300">Advanced</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="skill-bar bg-primary-600 h-2.5 rounded-full" style="width: 88%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="font-medium">Big Data (Spark, Hadoop)</span>
                                <span class="text-gray-600 dark:text-gray-300">Intermediate</span>
                            </div>
                            <div class="w-full bg-gray-200 dark:bg-gray-700 rounded-full h-2.5">
                                <div class="skill-bar bg-primary-600 h-2.5 rounded-full" style="width: 80%"></div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Tools & Technologies -->
                <div>
                    <h3 class="text-xl font-semibold mb-6 flex items-center">
                        <i class="fas fa-tools text-primary-600 dark:text-primary-400 mr-3"></i> Tools & Technologies
                    </h3>
                    <div class="grid grid-cols-3 gap-4">
                        <div class="bg-white dark:bg-gray-700 p-4 rounded-lg shadow-sm flex flex-col items-center tool-icon">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/1200px-Python-logo-notext.svg.png" 
                                 alt="Python" 
                                 class="h-10 w-10 object-contain mb-2">
                            <span class="text-sm font-medium dark:text-gray-200">Python</span>
                        </div>
                        <div class="bg-white dark:bg-gray-700 p-4 rounded-lg shadow-sm flex flex-col items-center tool-icon">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Jupyter_logo.svg/1200px-Jupyter_logo.svg.png" 
                                 alt="Jupyter" 
                                 class="h-10 w-10 object-contain mb-2">
                            <span class="text-sm font-medium dark:text-gray-200">Jupyter</span>
                        </div>
                        <div class="bg-white dark:bg-gray-700 p-4 rounded-lg shadow-sm flex flex-col items-center tool-icon">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2d/Tensorflow_logo.svg/1200px-Tensorflow_logo.svg.png" 
                                 alt="TensorFlow" 
                                 class="h-10 w-10 object-contain mb-2">
                            <span class="text-sm font-medium dark:text-gray-200">TensorFlow</span>
                        </div>
                        <div class="bg-white dark:bg-gray-700 p-4 rounded-lg shadow-sm flex flex-col items-center tool-icon">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/10/PyTorch_logo_icon.svg/1200px-PyTorch_logo_icon.svg.png" 
                                 alt="PyTorch" 
                                 class="h-10 w-10 object-contain mb-2">
                            <span class="text-sm font-medium dark:text-gray-200">PyTorch</span>
                        </div>
                        <div class="bg-white dark:bg-gray-700 p-4 rounded-lg shadow-sm flex flex-col items-center tool-icon">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/Apache_Spark_logo.svg/1200px-Apache_Spark_logo.svg.png" 
                                 alt="Spark" 
                                 class="h-10 w-10 object-contain mb-2">
                            <span class="text-sm font-medium dark:text-gray-200">Spark</span>
                        </div>
                        <div class="bg-white dark:bg-gray-700 p-4 rounded-lg shadow-sm flex flex-col items-center tool-icon">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Postgresql_elephant.svg/1200px-Postgresql_elephant.svg.png" 
                                 alt="PostgreSQL" 
                                 class="h-10 w-10 object-contain mb-2">
                            <span class="text-sm font-medium dark:text-gray-200">PostgreSQL</span>
                        </div>
                        <div class="bg-white dark:bg-gray-700 p-4 rounded-lg shadow-sm flex flex-col items-center tool-icon">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/93/Amazon_Web_Services_Logo.svg/1200px-Amazon_Web_Services_Logo.svg.png" 
                                 alt="AWS" 
                                 class="h-10 w-10 object-contain mb-2">
                            <span class="text-sm font-medium dark:text-gray-200">AWS</span>
                        </div>
                        <div class="bg-white dark:bg-gray-700 p-4 rounded-lg shadow-sm flex flex-col items-center tool-icon">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fa/Microsoft_Azure.svg/1200px-Microsoft_Azure.svg.png" 
                                 alt="Azure" 
                                 class="h-10 w-10 object-contain mb-2">
                            <span class="text-sm font-medium dark:text-gray-200">Azure</span>
                        </div>
                        <div class="bg-white dark:bg-gray-700 p-4 rounded-lg shadow-sm flex flex-col items-center tool-icon">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Laravel.svg/1200px-Laravel.svg.png" 
                                 alt="Power BI" 
                                 class="h-10 w-10 object-contain mb-2">
                            <span class="text-sm font-medium dark:text-gray-200">Power BI</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section id="education" class="py-20 bg-white dark:bg-gray-800">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-3xl font-bold text-center mb-16">Education</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- USF -->
                <div class="bg-gray-50 dark:bg-gray-700 p-8 rounded-lg shadow-sm">
                    <div class="flex items-center mb-4">
                        <div class="bg-primary-100 dark:bg-primary-900 p-3 rounded-full mr-4">
                            <i class="fas fa-university text-primary-600 dark:text-primary-300"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold">University of South Florida</h3>
                            <p class="text-gray-600 dark:text-gray-300">Master of Science in Computer Science</p>
                            <p class="text-gray-500 dark:text-gray-400 text-sm">Aug 2023 - May 2025</p>
                        </div>
                    </div>
                    <div class="pl-16">
                        <h4 class="font-medium mb-2">Relevant Coursework:</h4>
                        <ul class="list-disc list-inside text-gray-600 dark:text-gray-300 space-y-1">
                            <li>Trustworthy Aspect and AI</li>
                            <li>Introduction to Artificial Intelligence</li>
                            <li>Foundation of Software Security</li>
                            <li>Affective Computing</li>
                            <li>Human Computer Interaction</li>
                        </ul>
                    </div>
                </div>
                
                <!-- REVA University -->
                <div class="bg-gray-50 dark:bg-gray-700 p-8 rounded-lg shadow-sm">
                    <div class="flex items-center mb-4">
                        <div class="bg-primary-100 dark:bg-primary-900 p-3 rounded-full mr-4">
                            <i class="fas fa-university text-primary-600 dark:text-primary-300"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-semibold">REVA University</h3>
                            <p class="text-gray-600 dark:text-gray-300">Bachelor of Science in Computer Science & Engineering</p>
                            <p class="text-gray-500 dark:text-gray-400 text-sm">Aug 2017 - July 2021 | GPA: 9.17/10</p>
                        </div>
                    </div>
                    <div class="pl-16">
                        <h4 class="font-medium mb-2">Relevant Coursework:</h4>
                        <ul class="list-disc list-inside text-gray-600 dark:text-gray-300 space-y-1">
                            <li>Python Programming</li>
                            <li>Big Data and Hadoop</li>
                            <li>Machine Learning and Applications</li>
                            <li>Virtualization and Cloud Computing</li>
                            <li>Database Management Systems</li>
                        </ul>
                    </div>
                </div>
            </div>
            
            <!-- Certifications -->
            <div class="mt-12">
                <h3 class="text-2xl font-semibold text-center mb-8">Certifications</h3>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="bg-gray-50 dark:bg-gray-700 p-6 rounded-lg shadow-sm flex items-start">
                        <div class="bg-primary-100 dark:bg-primary-900 p-3 rounded-full mr-4">
                            <i class="fas fa-certificate text-primary-600 dark:text-primary-300"></i>
                        </div>
                        <div>
                            <h4 class="font-semibold">Microsoft Azure Data Fundamentals</h4>
                            <p class="text-gray-600 dark:text-gray-300">Microsoft | May 2021</p>
                            <p class="text-gray-500 dark:text-gray-400 mt-2">Proficient in Azure data services including Azure SQL Database, Cosmos DB, and Data Lake Storage</p>
                        </div>
                    </div>
                    <div class="bg-gray-50 dark:bg-gray-700 p-6 rounded-lg shadow-sm flex items-start">
                        <div class="bg-primary-100 dark:bg-primary-900 p-3 rounded-full mr-4">
                            <i class="fas fa-certificate text-primary-600 dark:text-primary-300"></i>
                        </div>
                        <div>
                            <h4 class="font-semibold">Google Analytics Individual Qualification</h4>
                            <p class="text-gray-600 dark:text-gray-300">Google | August 2021</p>
                            <p class="text-gray-500 dark:text-gray-400 mt-2">Proficient in web traffic analysis, conversion tracking, and digital marketing analytics</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-gray-50 dark:bg-gray-800">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-3xl font-bold text-center mb-16">Get In Touch</h2>
            <div class="flex flex-col md:flex-row">
                <div class="md:w-1/2 mb-10 md:mb-0 md:pr-8">
                    <h3 class="text-xl font-semibold mb-6">Contact Information</h3>
                    <p class="text-gray-600 dark:text-gray-300 mb-8">
                        Feel free to reach out if you're looking for a data scientist, have a question, or just want to connect.
                    </p>
                    <div class="space-y-6">
                        <div class="flex items-start bg-white dark:bg-gray-700 p-4 rounded-lg">
                            <div class="bg-primary-100 dark:bg-primary-900 p-3 rounded-full mr-4">
                                <i class="fas fa-envelope text-primary-600 dark:text-primary-300"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold">Email</h4>
                                <p class="text-gray-600 dark:text-gray-300">msumanth00@gmail.com</p>
                            </div>
                        </div>
                        <div class="flex items-start bg-white dark:bg-gray-700 p-4 rounded-lg">
                            <div class="bg-primary-100 dark:bg-primary-900 p-3 rounded-full mr-4">
                                <i class="fas fa-phone-alt text-primary-600 dark:text-primary-300"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold">Phone</h4>
                                <p class="text-gray-600 dark:text-gray-300">+1 (656) 209-1703</p>
                            </div>
                        </div>
                        <div class="flex items-start bg-white dark:bg-gray-700 p-4 rounded-lg">
                            <div class="bg-primary-100 dark:bg-primary-900 p-3 rounded-full mr-4">
                                <i class="fas fa-map-marker-alt text-primary-600 dark:text-primary-300"></i>
                            </div>
                            <div>
                                <h4 class="font-semibold">Location</h4>
                                <p class="text-gray-600 dark:text-gray-300">Tampa, FL</p>
                            </div>
                        </div>
                    </div>
                    <div class="mt-10">
                        <h4 class="font-semibold mb-4">Follow Me</h4>
                        <div class="flex space-x-4">
                            <a href="#" class="bg-white dark:bg-gray-700 p-3 rounded-full text-gray-700 dark:text-gray-300 hover:bg-primary-100 dark:hover:bg-primary-900 hover:text-primary-600 dark:hover:text-primary-300 transition">
                                <i class="fab fa-linkedin-in"></i>
                            </a>
                            <a href="#" class="bg-white dark:bg-gray-700 p-3 rounded-full text-gray-700 dark:text-gray-300 hover:bg-primary-100 dark:hover:bg-primary-900 hover:text-primary-600 dark:hover:text-primary-300 transition">
                                <i class="fab fa-github"></i>
                            </a>
                            <a href="#" class="bg-white dark:bg-gray-700 p-3 rounded-full text-gray-700 dark:text-gray-300 hover:bg-primary-100 dark:hover:bg-primary-900 hover:text-primary-600 dark:hover:text-primary-300 transition">
                                <i class="fab fa-kaggle"></i>
                            </a>
                        </div>
                    </div>
                </div>
                <div class="md:w-1/2">
                    <form class="space-y-6" id="contact-form">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div>
                                <label for="name" class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-1">Name</label>
                                <input type="text" id="name" class="w-full px-4 py-3 border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-primary-500 outline-none transition bg-white dark:bg-gray-700" required>
                            </div>
                            <div>
                                <label for="email" class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-1">Email</label>
                                <input type="email" id="email" class="w-full px-4 py-3 border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-primary-500 outline-none transition bg-white dark:bg-gray-700" required>
                            </div>
                        </div>
                        <div>
                            <label for="subject" class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-1">Subject</label>
                            <input type="text" id="subject" class="w-full px-4 py-3 border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-primary-500 outline-none transition bg-white dark:bg-gray-700" required>
                        </div>
                        <div>
                            <label for="message" class="block text-sm font-medium text-gray-700 dark:text-gray-300 mb-1">Message</label>
                            <textarea id="message" rows="5" class="w-full px-4 py-3 border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-primary-500 outline-none transition bg-white dark:bg-gray-700" required></textarea>
                        </div>
                        <button type="submit" class="w-full bg-primary-600 text-white px-6 py-3 rounded-lg font-medium hover:bg-primary-700 transition focus:outline-none focus:ring-2 focus:ring-primary-500 focus:ring-offset-2">
                            Send Message
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-6 md:mb-0">
                    <span class="text-xl font-bold">Sumanth Medaramettala</span>
                    <p class="text-gray-400 mt-2">Data Scientist & AI Engineer</p>
                </div>
                <div class="flex space-x-6">
                    <a href="#" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-linkedin-in text-xl"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-github text-xl"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition">
                        <i class="fab fa-kaggle text-xl"></i>
                    </a>
                </div>
            </div>
            <div class="border-t border-gray-800 mt-10 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-400 text-sm mb-4 md:mb-0">
                    © 2023 Sumanth Medaramettala. All rights reserved.
                </p>
                <div class="flex space-x-6">
                    <a href="#" class="text-gray-400 hover:text-white text-sm transition">Privacy Policy</a>
                    <a href="#" class="text-gray-400 hover:text-white text-sm transition">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.getElementById('menu-toggle').addEventListener('click', function() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        });

        // Form submission handler
        document.getElementById('contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! I will get back to you soon.');
            this.reset();
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                // Close mobile menu if open
                const mobileMenu = document.getElementById('mobile-menu');
                if (!mobileMenu.classList.contains('hidden')) {
                    mobileMenu.classList.add('hidden');
                }
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add animation to elements when they come into view
        const observerOptions = {
            threshold: 0.1
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate-fadeIn');
                    entry.target.classList.remove('opacity-0');
                }
            });
        }, observerOptions);

        // Observe all sections
        document.querySelectorAll('section').forEach(section => {
            section.classList.add('opacity-0', 'transition-opacity', 'duration-500');
            observer.observe(section);
        });

        // Dark mode toggle
        const themeToggleBtns = document.querySelectorAll('#theme-toggle, #theme-toggle-mobile');
        
        // Check for saved user preference, if any, on load of the website
        if (localStorage.getItem('color-theme') === 'dark' || (!('color-theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
            document.documentElement.classList.add('dark');
        } else {
            document.documentElement.classList.remove('dark');
        }

        themeToggleBtns.forEach(btn => {
            btn.addEventListener('click', function() {
                // Toggle the 'dark' class on the html element
                document.documentElement.classList.toggle('dark');
                
                // Update localStorage
                if (document.documentElement.classList.contains('dark')) {
                    localStorage.setItem('color-theme', 'dark');
                } else {
                    localStorage.setItem('color-theme', 'light');
                }
            });
        });
    </script>
</body>
</html>
