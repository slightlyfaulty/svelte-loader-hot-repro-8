<script>
	import Apple from './Apple.svelte'

	const apples = ['🍏', '🍎', '🍏', '🍎', '🍏']

	setInterval(() => {
		for (let i = 0; i < apples.length; i++) {
			apples[i] = apples[i] === '🍏' ? '🍎' : '🍏'
		}
	}, 500)
</script>

{#each apples as apple}
	<Apple {apple} />
{/each}
