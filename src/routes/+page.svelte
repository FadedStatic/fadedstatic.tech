<script>
	import Particles from 'svelte-particles';
	import { loadFull } from 'tsparticles';
	import ParticlesJson from '../particles.json';
	import { loadPolygonPath } from 'tsparticles-path-polygon';

	import { Navbar, NavBrand } from 'flowbite-svelte';

	let particlesInit = async (engine) => {
		await loadPolygonPath(engine);
		await loadFull(engine);
	};
</script>

<div>
	<Particles id="tsparticles" style="" options={ParticlesJson} {particlesInit} />
	<Navbar>
		<NavBrand href="/">
			<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
				>Flowbite</span
			></NavBrand
		>
	</Navbar>
</div>
