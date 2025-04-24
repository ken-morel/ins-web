<script>
    // No external dependencies
    const effectiveDate = "2025-04-01";
</script>

<svelte:head>
    <title>IS - Terms of Service</title>
</svelte:head>

<div class="terms-container">
    <!-- Navigation -->
    <header class="terms-header">
        <div class="terms-nav">
            <div class="brand">
                <img src="/is_logo.png" alt="IS Logo" class="logo" />
                <span class="brand-name">Intranet of Schools</span>
            </div>
            <nav class="nav-links">
                <a href="/" class="nav-link">Home</a>
                <a href="/contact" class="nav-link">Contact</a>
            </nav>
        </div>
    </header>

    <!-- Main Content -->
    <main class="terms-content">
        <a href="/" class="back-link">← Back to Home</a>
        
        <h1>Terms of Service</h1>
        <p class="effective-date">Effective: {effectiveDate}</p>

        <!-- Sections -->
        {#each sections as section}
            <section class="terms-section">
                <h2>{section.title}</h2>
                {#if section.type === 'list'}
                    <ul class="terms-list">
                        {#each section.items as item}
                            <li>{item}</li>
                        {/each}
                    </ul>
                {:else}
                    <p>{section.content}</p>
                {/if}
            </section>
        {/each}
    </main>

    <!-- Footer -->
    <footer class="terms-footer">
        <div class="footer-content">
            <img src="/is_logo.png" alt="IS Logo" class="footer-logo" />
            <p class="footer-text">Bridging gaps, building futures</p>
            <div class="legal-links">
                <a href="/policy" class="legal-link">Privacy Policy</a>
                <a href="/terms" class="legal-link">Terms of Service</a>
            </div>
            <p class="copyright">© 2023 Intranet of Schools. All rights reserved.</p>
        </div>
    </footer>
</div>

<style>
    /* Base Styles */
    .terms-container {
        min-height: 100vh;
        display: flex;
        flex-direction: column;
    }

    .terms-header {
        background-color: #1e3a8a;
        padding: 1rem 0;
        box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }

    .terms-nav {
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 1rem;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .brand {
        display: flex;
        align-items: center;
        gap: 0.75rem;
    }

    .logo {
        height: 40px;
        width: 40px;
    }

    .brand-name {
        color: white;
        font-weight: 600;
        font-size: 1.25rem;
    }

    .nav-links {
        display: flex;
        gap: 1.5rem;
    }

    .nav-link {
        color: white;
        text-decoration: none;
        font-size: 0.9rem;
    }

    .terms-content {
        flex: 1;
        max-width: 800px;
        margin: 0 auto;
        padding: 2rem 1rem;
    }

    .back-link {
        display: inline-block;
        color: #1e3a8a;
        text-decoration: none;
        margin-bottom: 2rem;
    }

    h1 {
        color: #1e3a8a;
        font-size: 2rem;
        margin-bottom: 1rem;
    }

    .effective-date {
        color: #6b7280;
        margin-bottom: 2rem;
    }

    .terms-section {
        margin-bottom: 2.5rem;
        border-left: 3px solid #f59e0b;
        padding-left: 1rem;
    }

    h2 {
        color: #1e3a8a;
        font-size: 1.5rem;
        margin-bottom: 1rem;
    }

    .terms-list {
        padding-left: 1.5rem;
        color: #4b5563;
        line-height: 1.6;
    }

    .terms-list li {
        margin-bottom: 0.5rem;
    }

    .terms-footer {
        background-color: #1e3a8a;
        color: white;
        padding: 2rem 1rem;
        margin-top: auto;
    }

    .footer-content {
        max-width: 1200px;
        margin: 0 auto;
        text-align: center;
    }

    .footer-logo {
        height: 50px;
        margin-bottom: 1rem;
    }

    .footer-text {
        margin-bottom: 1rem;
    }

    .legal-links {
        display: flex;
        gap: 1.5rem;
        justify-content: center;
        margin-bottom: 1rem;
    }

    .legal-link {
        color: white;
        text-decoration: none;
    }

    .copyright {
        font-size: 0.875rem;
        color: #e5e7eb;
    }

    @media (max-width: 768px) {
        .terms-nav {
            flex-direction: column;
            gap: 1rem;
        }

        .nav-links {
            flex-wrap: wrap;
            justify-content: center;
        }

        h1 {
            font-size: 1.75rem;
        }

        h2 {
            font-size: 1.25rem;
        }
    }
</style>

<script context="module">
    // Terms content data
    export const sections = [
        {
            title: "1. Acceptance of Terms",
            content: "By accessing or using the Intranet of Schools (IS) platform, you agree to be bound by these Terms of Service."
        },
        {
            title: "2. User Responsibilities",
            type: "list",
            items: [
                "Provide accurate registration information",
                "Maintain account confidentiality",
                "Use platform for educational purposes only",
                "Obtain parental consent for minors"
            ]
        },
        // Add other sections following same structure
    ];
</script>