<script>
    import { fade } from 'svelte/transition';
    export const prerender = true;
    const team = [
        { 
            name: "Ken Morel",
            role: "Developer",
            nickname: "ama",
            emoji: "💻"
        },
        {
            name: "Tandjou Wilfred",
            role: "Operations",
            emoji: "⚙️"
        },
        {
            name: "Ange Merveille",
            role: "Design",
            emoji: "🎨"
        },
        {
            name: "Mballa Armel",
            role: "Team Leader",
            emoji: "👑"
        },
        {
            name: "Alajemba",
            role: "Economist",
            emoji: "📈"
        }
    ];
    const features = [
        { 
            icon: '📱', 
            title: "Real-Time Alerts",
            desc: "Instant notifications for attendance, grades, and behavior updates"
        },
        {
            icon: '🤝',
            title: "Triangular Communication",
            desc: "Seamless connection between teachers, parents, and students"
        },
        {
            icon: '🎓',
            title: "Performance Tracking",
            desc: "Monitor academic progress with AI-powered insights"
        }
    ];

    let currentStat = 0;
    const stats = [
        { value: "40%", label: "Dropout Rate" },
        { value: "24/7", label: "Support" },
        { value: "1000₣", label: "Premium Plan" }
    ];
</script>

<svelte:head>
    <title>IS - Intranet of Schools</title>
</svelte:head>

<div class="min-h-screen bg-gradient-to-b from-blue-50 to-white">
<nav class="sticky top-0 bg-white shadow-sm z-50">
        <div class="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <img src="/is_logo.png" alt="IS Logo" class="h-12 w-12" />
                <span class="text-xl font-bold text-blue-800">Intranet of Schools</span>
            </div>
            <div class="space-x-6">
                <a href="#features" class="text-gray-600 hover:text-blue-800">Features</a>
                <a href="#pricing" class="text-gray-600 hover:text-blue-800">Pricing</a>
                <a href="#team" class="text-gray-600 hover:text-blue-800">Team</a>
            </div>
        </div>
    </nav>
    <!-- Hero Section -->
    <header class="text-center py-20 px-4">
        <h1 class="text-5xl font-bold mb-6 text-blue-800">
            Bridging Gaps, <span class="text-orange-500">Building Futures</span>
        </h1>
        <p class="text-xl text-gray-600 mb-8 max-w-2xl mx-auto">
            Breaking the cycle of school disengagement through real-time communication
            and community support
        </p>
        <a href="https://intranet-of-schools.web.app" class="bg-orange-500 text-white px-8 py-3 rounded-full 
                      hover:bg-orange-600 transition-all">
            Get Started
        </a>
    </header>

    <!-- Stats Bar -->
    <div class="flex justify-center gap-8 mb-20 flex-wrap">
        {#each stats as stat}
            <div transition:fade class="text-center p-4">
                <div class="text-4xl font-bold text-blue-800">{stat.value}</div>
                <div class="text-gray-600">{stat.label}</div>
            </div>
        {/each}
    </div>

    <!-- Features Grid -->
    <section class="max-w-6xl mx-auto px-4 mb-28" id="features">
        <h2 class="text-3xl font-bold text-center mb-12 text-blue-800">
            How IS Transforms Education
        </h2>
        
        <div class="grid md:grid-cols-3 gap-8">
            {#each features as feature}
                <div class="p-6 bg-white rounded-xl shadow-lg hover:shadow-xl transition-shadow">
                    <div class="text-5xl mb-4">{feature.icon}</div>
                    <h3 class="text-xl font-semibold mb-2">{feature.title}</h3>
                    <p class="text-gray-600">{feature.desc}</p>
                </div>
            {/each}
        </div>
    </section>

    <!-- Pricing Section -->
    <section class="bg-blue-800 text-white py-16" id="pricing">
        <div class="max-w-4xl mx-auto px-4 text-center">
            <h2 class="text-3xl font-bold mb-8">Empower Your School</h2>
            <div class="grid md:grid-cols-2 gap-8">
                <div class="p-6 bg-white/10 rounded-xl">
                    <h3 class="text-2xl font-bold mb-4">Basic Plan</h3>
                    <p class="mb-6">Essential features for school connectivity</p>
                    <div class="text-4xl font-bold">Free</div>
                </div>
                
                <div class="p-6 bg-orange-500 rounded-xl">
                    <h3 class="text-2xl font-bold mb-4">Premium Plan</h3>
                    <p class="mb-6">Advanced tools including AI Support</p>
                    <div class="text-4xl font-bold">1000₣<span class="text-lg">/student</span></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Team Section -->
    
<section class="py-16 bg-white text-center">
        <div class="max-w-4xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-blue-800 mb-8">Get the IS App</h2>
            <div class="space-y-4">
                <p class="text-gray-600 mb-6">Available for Android devices</p>
                <a href="https://github.com/recordbreakersorg/ins/releases/download/v1.0.0-a1.dev3/app-release.apk" 
                   class="inline-block bg-green-500 text-white px-8 py-3 rounded-lg
                          hover:bg-green-600 transition-all shadow-lg hover:shadow-xl">
                    ↓ Download APK (v1.0.0-a1.dev3)
                </a>
                <p class="text-sm text-gray-500 mt-4">Size: 49.56 MB</p>
            </div>
            <div class="space-y-4">
                <p class="text-gray-600 mb-6">Website version also available</p>
                <a href="https://intranet-of-schools.web.app" 
                   class="inline-block bg-green-500 text-white px-8 py-3 rounded-lg
                          hover:bg-green-600 transition-all shadow-lg hover:shadow-xl">
                    Visit Website
                </a>
            </div>
        </div>
    </section>

    <!-- Enhanced Team Section -->
    <section id="team" class="py-16 bg-gray-50">
        <div class="max-w-6xl mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-blue-800">Meet The Record Breakers</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                {#each team as member}
                    <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition-shadow">
                        <div class="text-5xl mb-4 text-center">{member.emoji}</div>
                        <h3 class="text-xl font-semibold text-center">{member.name}</h3>
                        {#if member.nickname}
                            <p class="text-center text-gray-500 mb-2">{member.nickname}</p>
                        {/if}
                        <p class="text-center text-blue-600">{member.role}</p>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-blue-800 text-white py-8">
        <div class="max-w-6xl mx-auto px-4 text-center">
            <img src="/is_logo.png" alt="IS Logo" class="h-16 mx-auto mb-6" />
            <p class="mb-4">Bridging gaps, building futures</p>
            <div class="flex justify-center space-x-6 mb-4">
                <a href="/policy" class="hover:text-orange-400">Privacy Policy</a>
                <a href="/terms" class="hover:text-orange-400">Terms of Service</a>
                <a href="/contact" class="hover:text-orange-400">Contact</a>
            </div>
            <p class="text-sm text-blue-200">© 2025 Record Breakers. All rights reserved.</p>
        </div>
</div>

<style>
</style>