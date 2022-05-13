<script>
    import { onMount } from 'svelte';
    import * as SC from 'svelte-cubed';
    import * as THREE from 'three';
    import { SVGLoader } from 'three/examples/jsm/loaders/SVGLoader';
    import logo from '$lib/tktokpost.svg?raw';

    const svgLogo = new SVGLoader().parse(logo);

    let spin = 0;

    SC.onFrame(() => {
    spin += 0.003;
    });

    let y = 0;
    let x = Math.PI;
    let z = 0;
</script>

<SC.Canvas antialias alpha>
  <SC.Group scale={0.05} rotation={[x,y,z]}>
    {#each svgLogo.paths as logoPath}
        <SC.Mesh 
            material={new THREE.MeshToonMaterial({
                color: 'yellow',
                roughness: 0.1,
                metalness: 0.5
            })} 
            rotation={[0, spin, spin]}
            geometry={new THREE.ExtrudeGeometry(logoPath.toShapes(false), {
             depth: 10
            })}
        />
        {/each}
  </SC.Group>  
    <SC.PerspectiveCamera position={[8, -10, 8]} />
    <SC.AmbientLight intensity={.01} />
    <SC.DirectionalLight intensity={.4} position={[7,5,4]} />
    <SC.PointLight intensity ={.5} position={[2, 5, 2]} />
    <SC.OrbitControls />
</SC.Canvas>

<!-- <input type="text" bind:value={text} />-->

<style lang="scss">
    @import 'components';
</style>