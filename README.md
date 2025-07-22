<!DOCTYPE html>
<html lang="en" class="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DailyNews</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
    }
  </script>
</head>
<body class="bg-gray-100 dark:bg-gray-900 text-gray-900 dark:text-white">

  <!-- Header -->
  <header class="bg-white dark:bg-gray-800 shadow">
    <div class="container mx-auto px-4 py-4 flex justify-between items-center">
      <h1 class="text-2xl font-bold text-blue-600 dark:text-blue-400">DailyNews</h1>

      <!-- Mobile Menu Button -->
      <button onclick="toggleMenu()" class="md:hidden text-xl">&#9776;</button>

      <!-- Navbar -->
      <nav id="navMenu" class="hidden md:flex space-x-4">
        <a href="#" class="hover:text-blue-500">Home</a>
        <a href="#" class="hover:text-blue-500">World</a>
        <a href="#" class="hover:text-blue-500">Politics</a>
        <a href="#" class="hover:text-blue-500">Tech</a>
        <button onclick="openLogin()" class="bg-blue-600 text-white px-3 py-1 rounded">Login</button>
        <button onclick="toggleDarkMode()" class="bg-gray-300 dark:bg-gray-700 px-3 py-1 rounded">🌓</button>
      </nav>
    </div>
  </header>

  <!-- Hero -->
  <section class="bg-blue-600 dark:bg-blue-700 text-white py-20 text-center px-4">
    <h2 class="text-4xl font-bold">Get the Latest News Every Day</h2>
    <p class="text-lg mt-2">Stay informed with breaking headlines, expert analysis, and real-time updates.</p>
  </section>

  <!-- Articles -->
  <section class="container mx-auto px-4 py-10 grid grid-cols-1 md:grid-cols-3 gap-6">
    <article class="bg-white dark:bg-gray-800 p-5 rounded shadow">
      <h3 class="text-xl font-semibold">Global Markets React</h3>
      <p class="text-sm text-gray-600 dark:text-gray-400">World News</p>
      <p class="mt-2">Markets shifted as oil prices surged...</p>
    </article>
    <article class="bg-white dark:bg-gray-800 p-5 rounded shadow">
      <h3 class="text-xl font-semibold">AI Regulation Begins</h3>
      <p class="text-sm text-gray-600 dark:text-gray-400">Tech</p>
      <p class="mt-2">Big tech announces AI rules...</p>
    </article>
    <article class="bg-white dark:bg-gray-800 p-5 rounded shadow">
      <h3 class="text-xl font-semibold">Election 2025</h3>
      <p class="text-sm text-gray-600 dark:text-gray-400">Politics</p>
      <p class="mt-2">Everything to know about the election...</p>
    </article>
  </section>

  <!-- Footer -->
  <footer class="bg-gray-800 text-white text-center py-4">
    <p>&copy; 2025 DailyNews. All rights reserved.</p>
  </footer>

  <!-- Login Modal -->
  <div id="loginModal" class="hidden fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center">
    <div class="bg-white dark:bg-gray-800 p-6 rounded shadow w-80">
      <h2 class="text-2xl font-bold mb-4">Login</h2>
      <input type="text" placeholder="Email" class="w-full mb-3 p-2 rounded border dark:bg-gray-700" />
      <input type="password" placeholder="Password" class="w-full mb-3 p-2 rounded border dark:bg-gray-700" />
      <button class="bg-blue-600 text-white px-4 py-2 rounded w-full">Login</button>
      <p class="text-sm mt-2">No account? <span onclick="openSignup()" class="text-blue-500 cursor-pointer">Sign up</span></p>
      <button onclick="closeLogin()" class="mt-3 text-red-500">Close</button>
    </div>
  </div>

  <!-- Signup Modal -->
  <div id="signupModal" class="hidden fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center">
    <div class="bg-white dark:bg-gray-800 p-6 rounded shadow w-80">
      <h2 class="text-2xl font-bold mb-4">Sign Up</h2>
      <input type="text" placeholder="Email" class="w-full mb-3 p-2 rounded border dark:bg-gray-700" />
      <input type="password" placeholder="Password" class="w-full mb-3 p-2 rounded border dark:bg-gray-700" />
      <button class="bg-green-600 text-white px-4 py-2 rounded w-full">Create Account</button>
      <p class="text-sm mt-2">Already have an account? <span onclick="openLogin()" class="text-blue-500 cursor-pointer">Log in</span></p>
      <button onclick="closeSignup()" class="mt-3 text-red-500">Close</button>
    </div>
  </div>

  <!-- Scripts -->
  <script>
    const toggleMenu = () => {
      const nav = document.getElementById("navMenu");
      nav.classList.toggle("hidden");
    };

    const toggleDarkMode = () => {
      document.documentElement.classList.toggle("dark");
    };

    const openLogin = () => {
      document.getElementById("loginModal").classList.remove("hidden");
      document.getElementById("signupModal").classList.add("hidden");
    };

    const closeLogin = () => {
      document.getElementById("loginModal").classList.add("hidden");
    };

    const openSignup = () => {
      document.getElementById("signupModal").classList.remove("hidden");
      document.getElementById("loginModal").classList.add("hidden");
    };

    const closeSignup = () => {
      document.getElementById("signupModal").classList.add("hidden");
    };
  </script>

</body>
</html>

