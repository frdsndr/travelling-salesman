<script>
	import { Canvas } from '@threlte/core';

	// cameras
	import Persp from './cameras/Persp.svelte';

	// geometry
	import Cube from '$lib/components/Travel/models/Cube.svelte';
	import Floor from '$lib/components/Travel/models/Floor.svelte';
	import TreeSquare from '$lib/components/Travel/models/TreeSquare.svelte';
	import BushSquare from '$lib/components/Travel/models/BushSquare.svelte';

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
		<TreeSquare variant={0} position={{ x: 2, y: 0, z: 0 }} />
		<TreeSquare variant={1} position={{ x: -4, y: 0, z: 4 }} />
		<TreeSquare variant={2} position={{ x: 7, y: 0, z: 7 }} />
		<BushSquare size="large" variant={0} position={{ x: 4, y: 0, z: 7 }} />
		<BushSquare size="small" variant={0} position={{ x: 3, y: 0, z: 8 }} />
		<BushSquare size="small" variant={1} position={{ x: 8, y: 0, z: 3 }} />

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
