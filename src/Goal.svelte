<script>
  const sentinelChar = '!'
  let courseGoal = '' 

  $: hasSentinelChar = courseGoal.indexOf(sentinelChar) === -1 ? false : true 
</script>

<h1 class:highlight="{ hasSentinelChar }">My course goal is: { courseGoal }</h1>
<input type="text" bind:value="{ courseGoal }" />

<style>
h1 { 
  color: blue;
}

.highlight { 
  color: red;
}
</style>