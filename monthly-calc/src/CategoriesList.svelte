<script>
    import Category from './Category.svelte'

    export let categories = [];

    function addCategory(event) {
        console.log('Add Category');
    }

</script>

<div class="panel-categories">
    {#each categories as category}
        <Category {...category} on:AddExpense />
    {/each}
    <button on:click={addCategory}>
        <div class="category-command-add"><i class="fa-solid fa-plus"></i>Add Category</div>
    </button>
</div>