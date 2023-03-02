<script>
    const title = "JavaScript 입문과 웹 UI 개발";
</script>

<svelte:head>
    <title>{title}</title>
</svelte:head>

<main>
    <h1>{title}</h1>
    <slot></slot>
</main>