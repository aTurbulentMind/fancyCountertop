<script>
    import * as SC from 'svelte-cubed';
    import * as THREE from 'three';
    import * as PE from 'svelte-cannon';
    import Box from '$lib/Box.svelte'

    let count = 1;
</script>

<svelte:window on:click={() => (count += 1)} />

<PE.World gravity={[0, -7.8, 0]}>
<SC.Canvas antialias shadows>
    <PE.Body mass={0} rotation={[-Math.PI / 2, 0, 0]}>
        <PE.Plane />
    </PE.Body>
    <SC.Mesh 
        receiveShadow
        geometry={new THREE.PlaneGeometry(100, 100)}
        rotation={[-Math.PI / 2, 0, 0]}
        material={new THREE.MeshStandardMaterial({ color: 'grey'})}
    />
    {#each  {length: count} as _}
    <Box />
    {/each}
    <SC.DirectionalLight intensity={.8} position={[15,15,15]} shadow={{ mapSize: [2048, 2048]}} />
	<SC.DirectionalLight intensity={.6} position={[35,15,5]} color={'yellow'} shadow={{ mapSize: [2048, 2048]}} />
    <SC.AmbientLight intensity={.6} />
    <SC.PerspectiveCamera position={[2, 60, 45]} target={[0, 0, 0]} />
    <SC.OrbitControls />
</SC.Canvas>
</PE.World>