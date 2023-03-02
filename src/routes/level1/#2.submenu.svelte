<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p"
        crossorigin="anonymous">
    function submenuToggle(){
        document.querySelectorAll('.list-group')[0].classList.toggle('show');
    }

</script>

<svelte:head>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css"
          rel="stylesheet"
          integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3"
          crossorigin="anonymous">

    <title>submenu</title>
</svelte:head>

<nav class="navbar navbar-light bg-light">
    <div class="container-fluid">
        <span class="navbar-brand">Navbar</span>
        <button on:click={submenuToggle} class="navbar-toggler" type="button">
            <span class="navbar-toggler-icon"></span>
        </button>
    </div>
</nav>

<!--TODO: 3. TODO: `<ul class="list-group show">`에 show를 처음부터 추가했을 땐 toggle기능이 정상적으로 동작하지만, 추가하지 않았을 땐 속성 검사 시 show가 보이지 않음.-->

<ul class="list-group show">
    <li class="list-group-item">An item</li>
    <li class="list-group-item">A second item</li>
    <li class="list-group-item">A third item</li>
    <li class="list-group-item">A fourth item</li>
    <li class="list-group-item">And a fifth one</li>
</ul>

<style>
    .list-group{
        display: none;
    }
    .show{
        display: block;
    }
</style>
