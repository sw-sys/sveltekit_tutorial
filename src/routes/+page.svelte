<script>
    import Header from "./Header.svelte";
    let name =$state('Scott');
    // let name = 'Scott';

</script>


<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<Header {name} />

First name: <input type= "text" bind:value={name} />