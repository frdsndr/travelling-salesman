<script>
	import { Canvas } from '@threlte/core';

	// cameras
	import Persp from './cameras/Persp.svelte';

	// geometry
	import Cube from '$lib/components/Travel/models/Cube.svelte';
	import Floor from '$lib/components/Travel/models/Floor.svelte';
	import Tree from '$lib/components/Travel/models/trees/TreeLarge.svelte';

	// lighting
	import Lights from '$lib/components/Travel/lighting/Lights.svelte';

	// utilities
	import Helpers from '$lib/components/Travel/utils/Helpers.svelte';
</script>

<div>
	<Canvas>
		<!-- cameras -->
		<Persp />

		<!-- lighting -->
		<Lights />

		<!-- geometry -->
		<Floor />
		<Cube />
		<Tree />

		<!-- utilities -->
		<Helpers />
	</Canvas>
</div>

<style>
	div {
		height: 100%;
		width: 100%;
		min-height: 500px;
	}
</style>
