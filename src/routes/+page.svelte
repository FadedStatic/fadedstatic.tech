<script>
	import Particles from 'svelte-particles';
	import { loadFull } from 'tsparticles';
	import ParticlesJson from '../particles.json';
    import { loadPolygonPath } from 'tsparticles-path-polygon';

	let particlesInit = async (engine) => {
		await loadPolygonPath(engine);
		await loadFull(engine);
	};
</script>

<div>
	<Particles
		id="tsparticles"
		style=""
		options={ParticlesJson}
		{particlesInit}
	/>
</div>
