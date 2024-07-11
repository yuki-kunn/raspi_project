<script>
	import MySkill from '../component/skills.svelte';
	import MyProject from '../component/projects.svelte';
    let name = "ゆーき";
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
</style>

<main>
    <header>
        <h1>Yuki'sポートフォリオ</h1>
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
        <p>こんにちは、{name}(北陽悠生)です。エンジニア志望の学生で、主にWeb開発に興味があります。</p>
    </section>

    <MySkill></MySkill>

	<MyProject></MyProject>

    <section id="contact">
        <h2>お問い合わせ</h2>
        
    </section>

    <footer>
        <p>&copy; 2024 {name}. All rights reserved.</p>
    </footer>
</main>