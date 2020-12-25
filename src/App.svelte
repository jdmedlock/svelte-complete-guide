<script>
  import Goal from './Goal.svelte'
</script>

<h1>Assignment - Svelte.js - The Complete Guide</h1>
<h2>Section 2 - Base Syntax & Core Features</h2>

<p>Solve these tasks.</p>

<ol>
  <li>Add an input field that allows users to enter a course goal.</li>
  <li>Output the user input in a h1 tag.</li>
  <li>Color the output red (e.g. by adding a class) if it contains at least one exclamation mark.</li>
  <li>Put the h1 tag + output into a separate component to which you pass the user input</li>
</ol>
<Goal />

<style>
  h1 { 
    color: blue;
  }
</style>