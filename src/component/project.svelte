
<script>
    let projects = [
        { title: "プロジェクト1", description: "プロジェクトの説明。" },
        { title: "プロジェクト2", description: "プロジェクトの説明。" }
    ];
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

<section id="projects">
    <h2>プロジェクト一覧</h2>
    {#each projects as project}
        <div class="project">
            <h3>{project.title}</h3>
            <p>{project.description}</p>
        </div>
    {/each}
</section>
