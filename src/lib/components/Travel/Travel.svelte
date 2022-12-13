<script>
	import { Canvas, OrbitControls, T } from '@threlte/core';

	import Persp from './cameras/Persp.svelte';

	import Cube from '$lib/components/Travel/models/Cube.svelte';
	import Floor from '$lib/components/Travel/models/Floor.svelte';
	// lighting
	import Lights from '$lib/components/Travel/lighting/Lights.svelte';
</script>

<div>
	<Canvas>
		<!-- cameras -->
		<Persp />

		<!-- lighting -->
		<Lights />

		<!-- Geometry -->
		<Floor />
		<Cube />
	</Canvas>
</div>

<style>
	div {
		height: 100%;
		width: 100%;
		min-height: 500px;
	}
</style>
