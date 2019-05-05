<script>
	export let name;

	let count = 0;

	const proffessionArr = [
		{			
			'name': 'Daniel',
			'prof': 'Developer'
		},
		{			
			'name': 'Curry',
			'prof': 'Sunbather'
		}
	]

	function handleClick() {
		count += 1;
	}	
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {name}!</h1>

<button on:click={handleClick}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

{#if count > 3} 
<h2>We are getting there</h2>
{/if}

<ul>
	{#each proffessionArr as prof}
		<li>{prof.name} ({prof.prof})</li>
	{/each}
</ul>