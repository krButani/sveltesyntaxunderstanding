<script>
    import FBForm from "./FeedbackFrom.svelte";
    export let username = 'Butani'; // if we can't find username then default set

    const methodchangecount = (e) => {
        count = count+1;
    }
   $: count = 0;
</script>

<h1>Hi, {username}</h1>
<h2>Count: {count}</h2>

<FBForm on:changename on:countchange={methodchangecount} />
<style>
    h1 {
        text-align: center;
    }
</style>