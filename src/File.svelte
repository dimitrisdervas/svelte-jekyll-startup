<script>
	import Theme from './Theme.svelte';


	export let name;
	export let info;
	$: type = name.slice(name.lastIndexOf('.') + 1);
</script>

<style>
	span {
		padding: 0 0 0 1.5em;
		background: 0 0.1em no-repeat;
		background-size: 1em 1em;
	}
</style>

<span style="background-image: url(assets/svg/{type}.svg)">{name}{#if info != null } - {info}{/if}</span>

<span>{#if name == 'theme'}<Theme></Theme>{/if}</span>

		
	