<script>
    import { onMount } from 'svelte';
    import { fade, fly } from 'svelte/transition';

    let isVisible = false;

    onMount(() => {
        isVisible = true;
    });
</script>

<main class="min-h-screen bg-gradient-to-b from-gray-50 to-white pt-20">
    <!-- Hero Section -->
    <section class="px-4 py-20 md:py-32 max-w-7xl mx-auto">
        {#if isVisible}
            <div class="text-center" in:fade={{ duration: 1000 }}>
                <h1 class="text-4xl md:text-6xl font-bold mb-8">Our Features</h1>
                <p class="text-xl text-gray-600 max-w-3xl mx-auto">
                    Discover how Neothink's powerful features can transform your productivity
                </p>
            </div>
        {/if}
    </section>

    <!-- Features Grid -->
    <section class="px-4 py-24 bg-gray-50">
        <div class="max-w-7xl mx-auto">
            <div class="grid md:grid-cols-3 gap-12">
                {#if isVisible}
                    <!-- NeoTaskmaster Card -->
                    <div class="p-8 bg-white rounded-2xl shadow-sm hover:shadow-md transition-shadow" in:fly={{ y: 20, duration: 800, delay: 200 }}>
                        <div class="h-16 mb-6 flex items-center justify-center">
                            <img 
                                src="/neothink.pro logos/neotaskmaster-transpbg-highres.png" 
                                alt="NeoTaskmaster Logo" 
                                class="h-12 object-contain"
                            />
                        </div>
                        <h3 class="text-2xl font-semibold mb-4">NeoTaskmaster</h3>
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
                    <div class="p-8 bg-white rounded-2xl shadow-sm hover:shadow-md transition-shadow" in:fly={{ y: 20, duration: 800, delay: 400 }}>
                        <div class="h-16 mb-6 flex items-center justify-center">
                            <img 
                                src="/neothink.pro logos/neoplan-transpbg-highres.png" 
                                alt="NeoPlan Logo" 
                                class="h-12 object-contain"
                            />
                        </div>
                        <h3 class="text-2xl font-semibold mb-4">NeoPlan</h3>
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
                    <div class="p-8 bg-white rounded-2xl shadow-sm hover:shadow-md transition-shadow" in:fly={{ y: 20, duration: 800, delay: 600 }}>
                        <div class="h-16 mb-6 flex items-center justify-center">
                            <img 
                                src="/neothink.pro logos/neometrics-transpbg-highres.png" 
                                alt="NeoMetrics Logo" 
                                class="h-12 object-contain"
                            />
                        </div>
                        <h3 class="text-2xl font-semibold mb-4">NeoMetrics</h3>
                        <p class="text-gray-600 mb-6">Advanced analytics to measure your productivity. Gain insights and optimize your workflow.</p>
                        <ul class="space-y-3">
                            <li class="flex items-center text-sm text-gray-600">
                                <svg class="w-5 h-5 mr-3 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                                    <path d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"/>
                                </svg>
                                Detailed productivity reports
                            </li>
                            <li class="flex items-center text-sm text-gray-600">
                                <svg class="w-5 h-5 mr-3 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                                    <path d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"/>
                                </svg>
                                Workflow optimization tips
                            </li>
                        </ul>
                    </div>
                {/if}
            </div>
        </div>
    </section>
</main>

<style>
    main {
        font-family: 'Inter', sans-serif;
    }
</style>
