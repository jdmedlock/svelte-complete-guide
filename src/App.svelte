<script>
	import Signin from './Signin.svelte'
</script>

<h1>Assignment - Svelte.js - The Complete Guide</h1>
<h2>Section 3 - Working with Conditionals & Loops</h2>

<p>Solve these tasks.</p>

<ol>
	<li>Add a password input field and save the user input in a variable.</li>
	<li>Output "Too short" if the password is shorter than 5 characters and "Too long" if it's longer than 10.</li>
	<li>Output the password in a paragraph tag if it's between these boundaries.</li>
	<li>Add a button and let the user add the passwords to an array.</li>
	<li>Output the array values (= passwords) in a unordered list (ul tag).</li>
	<li>Bonus: If a password is clicked, remove it from the list.</li>
</ol>

<hr/>

<Signin />

<style>
	h1 {
		color: rgb(37, 122, 13);
	}
	
	h2 {
		color: rgb(104, 171, 86);
	}
</style>