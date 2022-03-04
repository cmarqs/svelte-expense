<script>
	import Head from "./Head.svelte";
	import CategoriesList from "./CategoriesList.svelte";
	import Input from "./Input.svelte";
	import Footer from "./Footer.svelte";
	import ExpensesList from "./ExpensesList.svelte";

	import categoryData from './Data/categories';
	let categories = [...categoryData];

	import expenseData from './Data/expenses';
	let expenses = [...expenseData];


	function AddExpense(event){
        const {id, name} = event.detail;

		console.log(`Notify fired! ${name}: ${id}`);


		// expenses.push();
    }
</script>

<main>
	<Head />
	<Input {AddExpense} />
	<CategoriesList categories={categories} on:AddExpense={AddExpense} />
	<ExpensesList expenses={expenses} />
	<Footer />
</main>

<style>
	main {
		text-align: center;
		padding: 0;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>