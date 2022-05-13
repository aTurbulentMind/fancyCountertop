<script>
    import * as THREE from 'three';
    import * as SC from 'svelte-cubed';
    import { spring } from 'svelte/motion';

    let width = 1;
    let height = 1;
    let depth = 1;
    

    let spin = 0;
    let isActive = false;

    let xPos = spring(0);
    $: $xPos = isActive ? 10 : 0;

    SC.onFrame(() => {
    spin += 0.001;
    });

    
</script>

    <div class="star-container">
    <SC.Canvas antialias alpha>
    <!--Object-->
    <SC.Mesh
            geometry={new THREE.TorusKnotGeometry()}
            position={[0, 0, 0]}
            rotation={[0, spin, spin]}
            scale={[width, height, depth]}
            material={new THREE.MeshToonMaterial({
                color: 'purple',
                roughness: 0.1,
                metalness: 0.5
            })} 
            />

    <!--Camera-->
    <SC.PerspectiveCamera position={[7,1,spin]} />
    
    <!--Lights-->
    <SC.AmbientLight intensity={.01} />
    <SC.DirectionalLight intensity={.4} position={[7,5,4]} />
    <SC.PointLight intensity ={.5} position={[2, 5, 2]} />
</SC.Canvas>
</div>

<style>
    .star-container{
        width: 100px;
        height: 100px;
        position: relative;
    }
</style>