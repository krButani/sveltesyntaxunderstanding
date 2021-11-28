<script>
    export let type = 'button';
    export let dclass= 'btn btn-primary';
</script>

<button type="{type}" class="{dclass}" on:click>
<slot></slot>
</button>
<style> 
.btn {
    margin: 0.5rem;
    padding: 0.5rem 1.2rem;
    border: none;
    border-radius: 5px;
    color: #fff;
}
.btn-primary {
    background-color: #FFB621;
}
</style>