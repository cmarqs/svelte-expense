<script>
import ExpenseItem from "./ExpenseItem.svelte";

export let expenses = [];
</script>

<div>
    <table>
        <thead>
            <th>Category</th>
            <th>Value</th>
        </thead>
        {#each expenses as expense}
            <ExpenseItem {...expense} />
        {/each}
    </table>
</div>

<style>
    table{
        width: 100%;
        color: black;
    }
</style>