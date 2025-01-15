<script>
  import { fade, fly } from 'svelte/transition';
  import { onMount } from 'svelte';
  
  let isVisible = false;
  let isScrolled = false;
  
  onMount(() => {
    isVisible = true;
    window.addEventListener('scroll', () => {
      isScrolled = window.scrollY > 20;
    });
  });
</script>

<!-- Navigation -->
<nav class="fixed w-full z-50 transition-all duration-200" class:shadow-sm={isScrolled} class:bg-white={isScrolled}>
  <div class="max-w-7xl mx-auto px-4 py-4 flex items-center justify-between">
    <div class="flex items-center">
      <img 
        src="/neothink.pro logos/neothinkpurp-transpbg-highres-removebg (1).png" 
        alt="Neothink Logo" 
        class="h-8 md:h-10"
      />
    </div>
    <div class="hidden md:flex items-center space-x-8">
      <a href="/features" class="text-gray-600 hover:text-gray-900">Features</a>
      <a href="/about" class="text-gray-600 hover:text-gray-900">About Us</a>
      <a href="/login" class="text-gray-600 hover:text-gray-900">Login</a>
      <a href="/signup" class="px-4 py-2 bg-black text-white rounded-full hover:bg-gray-800 transition-colors">
        Get Started
      </a>
    </div>
    <button class="md:hidden">
      <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M4 6h16M4 12h16M4 18h16" />
      </svg>
    </button>
  </div>
</nav>

<main class="min-h-screen bg-gradient-to-b from-gray-50 to-white pt-20">
  <!-- Hero Section -->
  <section class="px-4 py-20 md:py-32 max-w-7xl mx-auto">
    {#if isVisible}
      <div class="text-center" in:fade={{duration: 1000}}>
        <div class="mb-8">
          <img 
            src="/neothink.pro logos/neothinkpurp-transpbg-highres-removebg (1).png" 
            alt="Neothink Logo" 
            class="h-16 md:h-20 mx-auto mb-6"
          />
        </div>
        <h1 class="text-5xl md:text-7xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-purple-600 to-blue-500 leading-tight">
          Your Productivity,<br/>Amplified by AI
        </h1>
        <p class="mt-8 text-xl text-gray-700 max-w-3xl mx-auto leading-relaxed">
          Experience the next evolution of personal productivity. Neothink seamlessly combines AI intelligence with intuitive management for unparalleled efficiency.
        </p>
        <div class="mt-12 flex flex-col md:flex-row items-center justify-center gap-6">
          <a href="/signup" class="px-8 py-4 bg-purple-600 text-white rounded-full text-lg font-medium hover:bg-purple-700 transition-colors w-full md:w-auto">
            Get Started for Free
          </a>
          <a href="#demo" class="px-8 py-4 border border-gray-200 rounded-full text-lg font-medium hover:bg-gray-50 transition-colors w-full md:w-auto">
            Watch Demo
          </a>
        </div>
      </div>
    {/if}
  </section>

  <!-- Features Grid with enhanced styling -->
  <section id="features" class="px-4 py-24 bg-gray-50">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-5xl font-bold text-center mb-20">Supercharge Your Workflow</h2>
      <div class="grid md:grid-cols-3 gap-12">
        {#if isVisible}
          <!-- NeoTaskmaster Card -->
          <div class="p-8 bg-white rounded-2xl shadow-sm hover:shadow-md transition-shadow" in:fly={{y: 20, duration: 800, delay: 200}}>
            <div class="h-16 mb-6 flex items-center justify-center">
              <img 
                src="/neothink.pro logos/neotaskmaster-transpbg-highres.png" 
                alt="NeoTaskmaster Logo" 
                class="h-12 object-contain"
              />
            </div>
            <p class="text-gray-600 mb-6">AI-powered task management that adapts to your workflow. Automatically prioritizes and organizes your tasks.</p>
            <ul class="space-y-3">
              <li class="flex items-center text-sm text-gray-600">
                <svg class="w-5 h-5 mr-3 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"/>
                </svg>
                Smart task prioritization
              </li>
              <li class="flex items-center text-sm text-gray-600">
                <svg class="w-5 h-5 mr-3 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"/>
                </svg>
                Automated scheduling
              </li>
            </ul>
          </div>

          <!-- NeoPlan Card -->
          <div class="p-8 bg-white rounded-2xl shadow-sm hover:shadow-md transition-shadow" in:fly={{y: 20, duration: 800, delay: 400}}>
            <div class="h-16 mb-6 flex items-center justify-center">
              <img 
                src="/neothink.pro logos/neoplan-transpbg-highres.png" 
                alt="NeoPlan Logo" 
                class="h-12 object-contain"
              />
            </div>
            <p class="text-gray-600 mb-6">Strategic planning reimagined with AI. Turn your ideas into actionable project roadmaps.</p>
            <ul class="space-y-3">
              <li class="flex items-center text-sm text-gray-600">
                <svg class="w-5 h-5 mr-3 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"/>
                </svg>
                AI project planning
              </li>
              <li class="flex items-center text-sm text-gray-600">
                <svg class="w-5 h-5 mr-3 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"/>
                </svg>
                Smart milestone tracking
              </li>
            </ul>
          </div>

          <!-- NeoMetrics Card -->
          <div class="p-8 bg-white rounded-2xl shadow-sm hover:shadow-md transition-shadow" in:fly={{y: 20, duration: 800, delay: 600}}>
            <div class="h-16 mb-6 flex items-center justify-center">
              <img 
                src="/neothink.pro logos/neometrics-transpbg-highres.png" 
                alt="NeoMetrics Logo" 
                class="h-12 object-contain"
              />
            </div>
            
            <p class="text-gray-600 mb-6">Advanced analytics and insights to track your productivity and optimize your workflow.</p>
            <ul class="space-y-3">
              <li class="flex items-center text-sm text-gray-600">
                <svg class="w-5 h-5 mr-3 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"/>
                </svg>
                Productivity analytics
              </li>
              <li class="flex items-center text-sm text-gray-600">
                <svg class="w-5 h-5 mr-3 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"/>
                </svg>
                AI-powered insights
              </li>
            </ul>
          </div>
        {/if}
      </div>
    </div>
  </section>

  <!-- Social Proof -->
  <section class="px-4 py-20">
    <div class="max-w-7xl mx-auto text-center">
      <h2 class="text-3xl font-bold mb-12">Launching March 31st 2025</h2>
      <div class="grid grid-cols-2 md:grid-cols-4 gap-8 items-center opacity-60">
        <!-- Add company logos here -->
      </div>
    </div>
  </section>

  <!-- CTA Section -->
  <section class="px-4 py-20 bg-black text-white">
    <div class="max-w-4xl mx-auto text-center">
      <h2 class="text-3xl md:text-4xl font-bold mb-6">Ready to think differently?</h2>
    <p class="text-xl mb-10 text-gray-300">Be among the first to experience the future of personal productivity. Pre-register now and get early access when we launch in a few months. To Join the Beta</p>
      <a href="/signup" class="inline-block px-8 py-4 bg-white text-black rounded-full text-lg font-medium hover:bg-gray-100 transition-colors">
        Start Now
      </a>
    </div>
  </section>
</main>

<style>
  :global(body) {
    margin: 0;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  }

  /* Add smooth scroll behavior */
  :global(html) {
    scroll-behavior: smooth;
  }
</style>
