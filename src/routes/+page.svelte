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

<style>
	@import '../styles.css';
</style>

<div>
	<Particles id="tsparticles" style="" options={ParticlesJson} {particlesInit} />
	<Navbar class="bg-navbar">
		<NavBrand href="/">
			<span>
				FadedStatic.tech
			</span>
		</NavBrand>
	</Navbar>
</div>
