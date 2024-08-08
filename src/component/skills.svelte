<script>
    let skills = ["HTML", "CSS", "JavaScript", "Python", "PHP"];
</script>

<style>
    section {
        padding: 20px;
        margin: 20px;
        background: #fff;
        border-radius: 5px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
</style>

<section id="skills">
    <h2>スキルセット</h2>
    <ul>
        {#each skills as skill}
            <li>{skill}</li>
        {/each}
    </ul>
</section>