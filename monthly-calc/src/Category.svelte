<script>
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher(); 

    export let id, icon, name = {};
</script>

<button on:click={() => dispatch('AddExpense', {id, name})}>
    <div class="category-item"><i class="fa-solid fa-{icon}"></i>{name}</div>
</button>