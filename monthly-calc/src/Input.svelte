<script>
    let value = null;

    export let AddExpense;

    function handleValueExpense() {
        AddExpense({value});
    }
</script>

<div class="panel-input">
    <input type="number" id="txtInputExpense" bind:value={value} />
</div>
