<script>
    let name = "あなたの名前";
    let projects = [
        { title: "プロジェクト1", description: "プロジェクトの説明。" },
        { title: "プロジェクト2", description: "プロジェクトの説明。" }
    ];
    let skills = ["HTML", "CSS", "JavaScript", "その他のスキル"];
    let contactForm = { name: "", email: "", message: "" };

    function submitForm() {
        alert(`名前: ${contactForm.name}\nメールアドレス: ${contactForm.email}\nメッセージ: ${contactForm.message}`);
    }
</script>

<style>
    body {
        font-family: Arial, sans-serif;
        line-height: 1.6;
        margin: 0;
        padding: 0;
        background-color: #f4f4f4;
    }

    header {
        background: #333;
        color: #fff;
        padding: 1em 0;
        text-align: center;
    }

    header h1 {
        margin: 0;
    }

    nav ul {
        list-style: none;
        padding: 0;
    }

    nav ul li {
        display: inline;
        margin-right: 10px;
    }

    nav ul li a {
        color: #fff;
        text-decoration: none;
    }

    section {
        padding: 20px;
        margin: 20px;
        background: #fff;
        border-radius: 5px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }

    footer {
        text-align: center;
        padding: 20px;
        background: #333;
        color: #fff;
        bottom: 0;
        width: 100%;
    }

    form label {
        display: block;
        margin: 10px 0 5px;
    }

    form input, form textarea {
        width: 100%;
        padding: 10px;
        margin-bottom: 10px;
        border: 1px solid #ccc;
        border-radius: 5px;
    }

    form button {
        padding: 10px 20px;
        border: none;
        background: #333;
        color: #fff;
        cursor: pointer;
        border-radius: 5px;
    }

    form button:hover {
        background: #555;
    }
</style>

<main>
    <header>
        <h1>私のポートフォリオ</h1>
        <nav>
            <ul>
                <li><a href="#about">自己紹介</a></li>
                <li><a href="#projects">プロジェクト</a></li>
                <li><a href="#skills">スキルセット</a></li>
                <li><a href="#contact">お問い合わせ</a></li>
            </ul>
        </nav>
    </header>

    <section id="about">
        <h2>自己紹介</h2>
        <p>こんにちは、{name}です。エンジニア志望の学生で、主にWeb開発に興味があります。</p>
    </section>

    <section id="projects">
        <h2>プロジェクト</h2>
        {#each projects as project}
            <div class="project">
                <h3>{project.title}</h3>
                <p>{project.description}</p>
            </div>
        {/each}
    </section>

    <section id="skills">
        <h2>スキルセット</h2>
        <ul>
            {#each skills as skill}
                <li>{skill}</li>
            {/each}
        </ul>
    </section>

    <section id="contact">
        <h2>お問い合わせ</h2>
        <form on:submit|preventDefault={submitForm}>
            <label for="name">名前:</label>
            <input type="text" id="name" bind:value={contactForm.name} required>
            
            <label for="email">メールアドレス:</label>
            <input type="email" id="email" bind:value={contactForm.email} required>
            
            <label for="message">メッセージ:</label>
            <textarea id="message" bind:value={contactForm.message} required></textarea>
            
            <button type="submit">送信</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2024 {name}. All rights reserved.</p>
    </footer>
</main>