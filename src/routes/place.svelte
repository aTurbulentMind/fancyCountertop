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
    spin += 0.003;
    });
</script>


<div class="controls">
    <label> Width:</label>
    <input type="range" min={(0.1)} max={(3)} step={(0.1)} bind:value= {width} />

    <label> Height:</label>
    <input type="range" min={(0.1)} max={(3)} step={(0.1)} bind:value= {height} />
    
    <label> Depth:</label>
    <input type="range" min={(0.1)} max={(3)} step={(0.1)} bind:value= {depth} />
</div>

<SC.Canvas antialias shadows>

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
            castShadow
            />

    <!--Plane-->   
    <SC.Group position={[0, -3, 0]}>
        <SC.Mesh 
            receiveShadow
            geometry={new THREE.PlaneGeometry(100, 100)}
            material={new THREE.MeshStandardMaterial({color: 'grey'})}
            rotation={[-Math.PI / 2, 0, 0]}
            />
        <SC.Primitive 
            position={[0, 0.001, 0]}
            object={new THREE.GridHelper(100, 100, 'blue', 'green')}
        />
    </SC.Group>

    <!--Camera-->
    <SC.PerspectiveCamera position={[spin,1,7]} />
    <SC.OrbitControls />

    <!--Lights-->
    <SC.AmbientLight intensity={.01} />
    <SC.DirectionalLight shadow={{ mapSize: [2048, 2048]}} intensity={.4} position={[7,5,4]} />
    <SC.PointLight shadow={{ mapSize: [2048, 2048]}} intensity ={.5} position={[2, 5, 2]} />
</SC.Canvas>

<style>
    .controls{
        position: absolute;
        z-index: 10;
    }

    label{
        display: block;
        color: #fff;
    }
</style>