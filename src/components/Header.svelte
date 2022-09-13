<script>
    import {Router, Link } from "svelte-routing";
</script>

<header class="text-white body-font bg-gray-900">
    <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
      <a class="flex title-font font-medium items-center text-white mb-4 md:mb-0">
        <span class="ml-3 text-xl">Gtoste</span>
      </a>
      <nav class="md:ml-auto flex flex-wrap items-center justify-center">
        <nav>
            <Router>
                <Link to="/">Home</Link>
                <Link to="about">About</Link>
                <Link to="blog">Blog</Link>
                <Link to="board">Plansza</Link>
                <Link to="api">api</Link>
            </Router>
          </nav>
      </nav>
    </div>
</header>