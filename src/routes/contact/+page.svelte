<script>
    const teamMembers = [
        {
            name: "Engon Ken Morel",
            role: "Lead Developer",
            nickname: "Ama 🧑💻",
            contact: "ama.dev@intranetofschools.cm"
        },
        {
            name: "Tandjou Wilfred",
            role: "Operations Manager",
            contact: "wilfred.ops@intranetofschools.cm"
        },
        {
            name: "Ange Merveille",
            role: "UX Designer",
            contact: "ange.design@intranetofschools.cm"
        },
        {
            name: "Mballa Armel",
            role: "Team Leader",
            contact: "armel.lead@intranetofschools.cm"
        },
        {
            name: "Alajemba",
            role: "Business Strategist",
            contact: "alajemba.biz@intranetofschools.cm"
        }
    ];
</script>

<svelte:head>
    <title>IS - Contact Us</title>
</svelte:head>

<div class="contact-container">
    <!-- Header -->
    <header class="contact-header">
        <div class="header-content">
            <img src="/is_logo.png" alt="IS Logo" class="logo" />
            <h1>Contact The Record Breakers</h1>
            <p>Bridging communication gaps in Cameroonian education</p>
        </div>
    </header>

    <!-- Main Content -->
    <main class="contact-main">
        <!-- Contact Cards -->
        <section class="team-section">
            <h2>Our Team</h2>
            <div class="team-grid">
                {#each teamMembers as member}
                    <div class="member-card">
                        <div class="member-info">
                            <h3>{member.name}</h3>
                            {#if member.nickname}
                                <p class="nickname">{member.nickname}</p>
                            {/if}
                            <p class="role">{member.role}</p>
                            <a href={`mailto:${member.contact}`} class="email-link">
                                {member.contact}
                            </a>
                        </div>
                    </div>
                {/each}
            </div>
        </section>

        <!-- Contact Form -->
        <section class="form-section">
            <h2>Send Us a Message</h2>
            <form class="contact-form">
                <div class="form-group">
                    <label for="name">Your Name</label>
                    <input type="text" id="name" required />
                </div>
                
                <div class="form-group">
                    <label for="email">Your Email</label>
                    <input type="email" id="email" required />
                </div>

                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" rows="5" required></textarea>
                </div>

                <button type="submit" class="submit-button">
                    Send Message
                </button>
            </form>
        </section>

        <!-- Location -->
        <section class="location-section">
            <h2>Our Location</h2>
            <div class="map-wrapper">
                <iframe 
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3980.634321568051!2d11.485276814757844!3d3.848570197213367!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x108bc9a3119417a7%3A0x0!2zM8KwNTAnNTQuOCJOIDExwrAyOScxOS42IkU!5e0!3m2!1sen!2scm!4v1623337654321!5m2!1sen!2scm"
                    class="map-iframe"
                    loading="lazy"
                    title="our location">
                </iframe>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="contact-footer">
        <p>© 2023 Intranet of Schools - Bridging Educational Gaps in Cameroon</p>
    </footer>
</div>

<style>
    .contact-container {
        font-family: 'Segoe UI', system-ui, sans-serif;
        line-height: 1.6;
        color: #2d3748;
    }

    .contact-header {
        background-color: #1e3a8a;
        color: white;
        padding: 2rem 1rem;
        text-align: center;
    }

    .header-content {
        max-width: 1200px;
        margin: 0 auto;
    }

    .logo {
        height: 60px;
        margin-bottom: 1rem;
    }

    .contact-header h1 {
        font-size: 2.5rem;
        margin-bottom: 0.5rem;
    }

    .contact-header p {
        font-size: 1.1rem;
        opacity: 0.9;
    }

    .contact-main {
        max-width: 1200px;
        margin: 2rem auto;
        padding: 0 1rem;
    }

    .team-section h2,
    .form-section h2,
    .location-section h2 {
        font-size: 2rem;
        color: #1e3a8a;
        margin-bottom: 2rem;
        text-align: center;
    }

    .team-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 1.5rem;
        margin-bottom: 3rem;
    }

    .member-card {
        background: white;
        border-radius: 8px;
        padding: 1.5rem;
        box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        transition: transform 0.2s ease;
    }

    .member-card:hover {
        transform: translateY(-3px);
    }

    .member-info h3 {
        font-size: 1.25rem;
        margin-bottom: 0.25rem;
        color: #1e3a8a;
    }

    .nickname {
        font-style: italic;
        color: #4a5568;
        margin-bottom: 0.5rem;
    }

    .role {
        color: #4a5568;
        font-weight: 500;
        margin-bottom: 1rem;
    }

    .email-link {
        color: #2b6cb0;
        text-decoration: none;
        word-break: break-all;
    }

    .email-link:hover {
        text-decoration: underline;
    }

    .contact-form {
        background: white;
        padding: 2rem;
        border-radius: 8px;
        box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        margin-bottom: 3rem;
    }

    .form-group {
        margin-bottom: 1.5rem;
    }

    .form-group label {
        display: block;
        margin-bottom: 0.5rem;
        font-weight: 500;
    }

    .form-group input,
    .form-group textarea {
        width: 100%;
        padding: 0.75rem;
        border: 1px solid #cbd5e0;
        border-radius: 4px;
        font-size: 1rem;
    }

    .submit-button {
        background-color: #1e3a8a;
        color: white;
        padding: 0.75rem 1.5rem;
        border: none;
        border-radius: 4px;
        font-size: 1rem;
        cursor: pointer;
        transition: background-color 0.2s ease;
    }

    .submit-button:hover {
        background-color: #153061;
    }

    .map-wrapper {
        position: relative;
        padding-bottom: 56.25%;
        height: 0;
        margin-bottom: 3rem;
    }

    .map-iframe {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        border: none;
        border-radius: 8px;
    }

    .contact-footer {
        background-color: #1e3a8a;
        color: white;
        text-align: center;
        padding: 1rem;
        margin-top: 3rem;
    }

    @media (max-width: 768px) {
        .contact-header h1 {
            font-size: 2rem;
        }

        .team-grid {
            grid-template-columns: 1fr;
        }

        .contact-form {
            padding: 1rem;
        }
    }
</style>