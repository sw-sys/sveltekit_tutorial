<script lang="ts">
    import Header from "./Header.svelte";
    import { onMount } from "svelte";

    let name =$state('Scott');
    // define store opening variable
    let status: 'OPEN' | 'CLOSED' = $state('OPEN')

    // define status by current time
    const updateStatus = () => {
        const now = new Date();
        const hours = now.getUTCHours(); // get current hour in GMT
        status = hours >= 9 && hours < 17 ? "OPEN" : "CLOSED";
    }
    // logic to automatically update store opening status based on time
    onMount(() => {
        updateStatus();
        // define update interval - every minute
        const interval = setInterval(updateStatus, 60000);
        return () => clearInterval(interval); // clean component on unmount
    })

    // // Status button toggle
    // function onclick() {
    //     status = status === "OPEN" ? 'CLOSED' : 'OPEN';
    // }

</script>

<h1>Welcome to SvelteKit</h1>
<p class="text-green-400">Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<Header {name} />

<p>First name: <input type= "text" bind:value={name} /></p>

<p>The store is now {status}</p>

<!-- <button onclick={onclick}>Toggle Opening Status</button> -->
<!-- OR function below -->
<button onclick={() => {
    status = status === "OPEN" ? 'CLOSED' : 'OPEN';
}}>Toggle Opening Status</button>